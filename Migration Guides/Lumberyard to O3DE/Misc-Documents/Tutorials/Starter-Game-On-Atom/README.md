# StarterGame on Atom

### 1. Setup

#### 1.1. Requirements

- Python 3.7.5 or Python 3.8
- The project is currently utilizing Lumberyard 1.28. Any conversion tools are authored assuming 1.28. 
- Transitioning a Lumberyard project to O3DE is best performed utilizing a source code version of O3DE. This is available at https://github.com/o3de/o3de

#### 1.2. Project

If you are trying to run the Atom version of StarterGame, use the AtomStarterGame project.

If you are trying to convert a different project to use Atom, follow [Converting a Legacy Renderer Project](./../Converting-a-Legacy-Renderer-Project-to-an-Atom-Project) to an Atom Project to set up the Atom gems.

#### 1.3. Set AssetCatalog to Xml

Makes the asset catalog .xml instead of binary.

    Code\Tools\AssetProcessor\native\AssetManager\AssetCatalog.cpp line# 175 ST_BINARY → ST_XML

AssetCat Image

You must re-build lumberyard (just building the editor project should suffice) after unshelving this change, then delete dev\Cache\StarterGame\pc\startergame\assetcatalog.xml, run the AssetProcessor, and when it is finished, confirm that when you open assetcatalog.xml in a text editor, it shows up as readable .xml instead of a binary file. It's not necessary for running the project, but the conversion scripts depend on being able to parse the asset catalog.

#### 1.4. Conversion Scripts Location

All these files are located in origin/main Gems/AtomLyIntegration/CommonFeatures/Assets/Editor/Scripts/LegacyContentConversion.

#### 1.5. Python Dependencies

Type '*python*' on the command line to see which version of python you are using. See the required python version in the **Requirements** section above.

To use the python distributed with Lumberyard, you can point your PATH to Lumberyard\python which should contain the python and pip command. **Note:** an external locally installed python will work so long as the dependencies below are installed and that the version is correct.

Install python dependencies in the following in order:

    pip install numpy
    pip install pillow
    pip install libtiff
    pip install python-box

### 2. Legacy Component Conversion

####2.1. Run Material Conversion

*Legacy Asset Conversion Utility (StarterGame) page*

#### 2.2. Fix Material Paths

The legacy renderer allows materials to have invalid paths that refer to a location where there is no texture. In Atom, this will result in a material failing to process. Before running the component conversion, all materials and models must successfully process, so they can be added to the asset catalog. After you have fixed the paths in the .mtl files and added any missing textures, you can re-run the material conversion so the atom materials will refer to the correct textures.

#### 2.3. Run Component Conversion

In the Lumberyard engine root folder, run:

    python Gems/AtomLyIntegration/CommonFeatures/Assets/Editor/Scripts/LegacyContentConversion/LegacyComponentConverter.py "-project=AtomStarterGame -include_gems -use_p4"

- **note:** the -use_p4 flag can be omitted if on git. this option will attempt to automatically checkout the file to be converted, so it's not read only. If the file to be converted is read only, the conversion will fail.
- **note:** using -include_gems will check out and convert all the .slice/.layer/.ly/.cry files in the project and the Gems folder, even for gems that aren't enabled by the project. So you will need to revert changes to gems you do not wish to convert
- All the options need to be in one big "`<insert all your options here>`" because the script is going to split that string using the - character.

#### 2.3.1. Sample: Converting a slice file containing a legacy mesh component

Pre conversion
Image

After conversion
Image

### 3. Open Legacy Level (Ex: StarterGame)

The level is called Game/SinglePlayer.ly. This was changed in 1.25. The old level that's called StarterGame will be empty and grey with some auxgeom stuff but no models.

You will have to add create an entity and add a Global Skylight (IBL) component or some other lighting for the level to be lit. Otherwise, the objects are going to appear black. You could also add other lights, but IBL is the easiest way. You can use examplediffusehdr_cm_ibldiffuse and examplediffusehdr_cm_iblspecular, since those already exist in the Atom_Features_Common gem.

Then just run the Editor. The level will take a few minutes to load, even on desktop; longer than legacy. You'll see a white window where any (ignorable) errors/warnings will appear.

There will be a bunch of red 'invisible' walls.

- These red walls are physics colliders which have been baked into the FBX.  You'll need to open the FBX setting files using Asset Browser and make sure the phys-mesh is used only for PhysX and not rendering.

If you see a copper material, that means it's something where the conversion script couldn't find the right material to use. The level hasn't been exported, and hasn't been tested in the launcher, so your mileage may vary. Trying to save the level after you open it hasn't been tested and might crash.

Some materials may be black in areas, use Photoshop to make sure opaque materials aren't using any alpha in their base texture.  There's a bug causing base texture maps to use premultiplied alpha.


### 4. Potential Improvements

#### 4.1.1. Find the best solution for diffuse with something in the alpha channel

For simplicity, when I encounter a diffuse texture with an alpha channel, which does not work properly in Atom, I create a new _basecolor texture without the alpha. It would be better if the diffuse color just worked. Possibly by creating a .imagsettings file with the appropriate settings instead of creating a new texture. And we might want to keep that alpha channel if Atom supports the same thing it was used for in legacy.

#### 4.1.2. Test level saving

Right now, you can run the level in the editor after converting and it works. But it remains to be seen if saving then re-opening the level works.

#### 4.1.3. Find better solution for no-draw materials

Right now the material conversion always makes a new no-draw material when it encounters a no-draw physics proxy material. Ideally, we should only be using one shared no-draw material for physics proxies, but the conversion process would need to change for the mesh conversion to become aware of the no-draw materials. Additionally, there are some entities ('invisible walls in startergame') where the current hack doesn't even work.

#### 4.1.4. Convert other Atom components

Now that the framework is there for meshes and materials, it would be straightforward to replace legacy light entities with an atom equivalent or at least an approximation. It would also be good to create Atom post-processing components or other types.

#### 4.1.5. Better logging

It would be helpful to have one place where it's clear what exactly got converted, another place that calls out exactly what was not able to be converted, etc.

#### 4.1.6. Tests

If this were to be a real feature of Atom, each piece of functionality could be tested using Hydra (Editor Python Testing), rather than just observing that it seems to work on my machine.

#### 4.1.7. Use AzLmbr

Running a python file from the command line that uses azlmbr module is not straightforward. So instead, I'm parsing the asset catalog to roll my own functionality that would normally come via asset system ebus calls. It still works as-is, just extra setup time. But there is also a hard-coded path to the asset catalog that needs to be updated for each project, though that could be fixed independently of using azlmbr.

#### 4.1.8. Relative paths

There is at least one place where I'm assuming relative paths will be in the same project/gem folder as the thing that's being converted, but that's not necessarily true.

#### 4.1.9. Serialization formatting

The script writes all the added xml in a single line, instead of putting each element on a new line like AzCore serialization. As it stands, if you don't open and re-save the slice/level/layer files, they'll have a formatting difference that will persist until the next person comes along and tries to modify the slice/level/layer. Not a big deal, but that next person would probably be confused as to why a part of the file that is seemingly unrelated changed, and would increase the chance of merge conflicts. Might not be an issue if no one is diff'ing or merging these files to begin with.

#### 4.1.10. Better Default Material

Right now, by default the script adds a copper material when it can't find an equivalent match to what legacy uses. It would be better if it were a specific 'ConversionDefault' material included with the script that was bright and easy to spot (lime green emissive). But it would also be good to include a script/converter that strips this default material and/or points out where it's been applied, so people can make sure they clean up any instances they did not catch.

During the test and review of the material conversion script a bit during the current LBC week. Here are the notes I collected about more we need to do to get these scripts in a good state for customers.

1. Scripts need to be centrally located, not in AtomTest project.
2. Would be nice to have a usage statement when running the scripts with no command line arguments.
3. For "conversion not supported" we should report the reason why conversion wasn't supported.
4. Conversion probably needs to unpack roughness from the alpha channel of ddna maps. Currently, it apparently defaults to "EngineAssets/TextureMsg/DefaultNoUVs_spec.tif". Or we need to update Atom to support packing ddna.
5. The material conversion should probably not save values when default values would be appropriate. For example, don't output "specularF0":{ "factor": 1.0,"useTexture": false,"textureMap": ""},
6. Some fields are outdated and will fail to build the resulting .material file. For example, "useBaseColorTextureAlpha" has been replaced with "opacityMode". We need to go through and update everything to work with the latest version of StandardPBR.
7. Legacy materials may refer to the product .dds files rather than source files. If they reference dds then we probably need to replace that with the source file type. Or we could make the material builder automatically switch the extension and report a warning.
8. We need hair, skin, and eye shaders. Or at least some way to map those into a StandardPBR.
9. We should have regression tests for these scripts if we are going to support them, to make sure it stays in sync with the material type definitions.
10. I would make AtomMaterial a lot more general, less smart. It shouldn't try to understand the correlation between different properties. It should just make it easit to set/get property values. The smarts should all be in the Material_File.convert() function.
11. It's not clear whether P4 integration is working. It didn't mark-for-add any of the new files it created. But the files I was converting weren't checked into P4 so that might be causing it to skip adding the new files?
12. We need to add git support since we're switching the whole engine to git. But still need to maintain P4 support because our customers might continue using that?



##### Updated Aug 2022