# SerializeContextTools Conversion Scripts

This page contains windows cmd scripts for invoking the SerializeContextTools.exe application to convert ObjectStream files into Json files compatible with the Settings Registry

### Conversion Script for *.physicsconfiguration / *.physxconfiguration files

The following script can be run to convert *.physicsconfiguration and *.physconfiguration files over to a ${project}/Registry/physicsconfiguration.setreg and ${project}/Registry/physxconfiguration.setreg respectively

**Ex. Convert Game Projects phys*conversion.setreg file**
`REM The The parameter to the convert_physxconfiguration.cmd script is for a directory containing a SerializeContextTools.exe application`
`convert_physxconfiguration.cmd windows_vs2019/bin/profile`

convert_physxconfiguration.cmd (Link to Scripts file)

### Convert Editor.xml/Game.xml over to ${Project}/Registry/*.setreg

Script: convert_editor_game_xml.cmd (Link to Scripts file)

This script is for taking an Editor.xml/Game.xml from a game project ${Project}/Config/ directory and generating three settings registry for each `[${Project}, <Editor|Game>]` combination.

**Ex. Converting Lumberyard projects Editor/Game.xml over to *.setreg**
REM The The parameter to the convert_physxconfiguration.cmd script is for a directory containing a SerializeContextTools.exe application
convert_editor_game_xml.cmd windows_vs2019/bin/profile

For example converting just the StarterGame project Config/Editor.xml and Config/Game.xml results in the following files
<table>
  <tr>
    <th>SerializeContextTools Command</th>
    <th>Result Settings Registry File</th>
  </tr>
  <tr>
    <td>windows_vs2019/bin/profile/SerializeContextTools.exe convertad --config=Config/Editor.xml --skipgems --json-prefix=/Amazon/AzCore --regset="/Amazon/AzCore/Bootstrap/sys_game_folder=StarterGame"</td>
    <td>StarterGame/Registry/memory.editor.setreg</td>
  </tr>
  <tr>
    <td>windows_vs2019/bin/profile/SerializeContextTools.exe convertad --config=Config/Editor.xml --skipsystem --json-prefix=/Amazon/Gems --regset="/Amazon/AzCore/Bootstrap/sys_game_folder=StarterGame"</td>
    <td>StarterGame/Registry/module.editor.setreg</td>
  </tr>
    <tr>
    <td>windows_vs2019/bin/profile/SerializeContextTools.exe convertad --config=Config/Game.xml --skipgems --json-prefix=/Amazon/AzCore --regset="/Amazon/AzCore/Bootstrap/sys_game_folder=StarterGame"</td>
    <td>StarterGame/Registry/memory.game.setreg</td>
  </tr>
    <tr>
    <td>windows_vs2019/bin/profile/SerializeContextTools.exe convertad --config=Config/Game.xml --skipsystem --json-prefix=/Amazon/Gems --regset="/Amazon/AzCore/Bootstrap/sys_game_folder=StarterGame"</td>
    <td>StarterGame/Registry/module.game.setreg<br>
Also generates setreg files with gem specific settings in:<br>
"`<GemSourcePath>/Registry/`" for each gem with a ModuleEntity within the Editor.xml/Game.xml</td>
  </tr>
</table>

##### Updated Aug 2022