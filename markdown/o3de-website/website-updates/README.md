# O3DE Website Updates

This is a guide to assit with common website updates for banners, color code changes, logo updates, etc. 

## Table Of Contents
  * [Banners](#banners)
  * [Color Codes](#color-codes)
  * [Member Logos](#member-logos)
  * [Image Updates](#image-updates)
  * [Menu Changes](#menu-changes)

## Banners



## Color Codes

To incorporate a new color to the website, the existing colors can be found in the website folder under `assets/sass` in the `custom.sass` file. The color codes are available around line 70 in a section. This section makes it easier to reference the color code instead of looking up the Hex code.

To add a new color, insert a new line under the `// Variables` section. For example:

If the existing section looks like this:

```
// Variables 

$font-family-headers: "Open Sans" 
$font-family-Poppins: "Poppins", sans-serif;
$o3de-black: #000
$o3de-white: #fff
$o3de-lightgray: #ddd
$o3de-blue: #1E70EB
$o3de-darkblue: #0F3876
$o3de-docsblue: #2A4875
$o3de-mediumblue: #4B8DEF
$o3de-lightblue: #A5C6F7
$o3de-blue-highlight: #94D2FF
$o3de-green: #58BD61
$o3de-purple: #700AC7
$o3de-aqua: #0AC1C7
```

Add a new line at the bottom and name it, such as `O3DE Pink`. Then, insert the color code for the new color.

```
// Variables 

$font-family-headers: "Open Sans" 
$font-family-Poppins: "Poppins", sans-serif;
$o3de-black: #000
$o3de-white: #fff
$o3de-lightgray: #ddd
$o3de-blue: #1E70EB
$o3de-darkblue: #0F3876
$o3de-docsblue: #2A4875
$o3de-mediumblue: #4B8DEF
$o3de-lightblue: #A5C6F7
$o3de-blue-highlight: #94D2FF
$o3de-green: #58BD61
$o3de-purple: #700AC7
$o3de-aqua: #0AC1C7
$o3de-pink: #f16dbb
```

As demonstrated, `$o3de-pink: #f16dbb` has been added to the code block. Consequently, one can use o3de-pink while designing, instead of using the Hex code.

After adding the $o3de-pink variable in the custom.sass file, we can use it to replace the color code in the banner section. Here's the updated code:

```
// banner
a.top-banner
  color: $o3de-pink
  background-color: rgba(112,10,199,0.9)
  display: block
  padding: 10px 0
  transition: .2s ease
  box-shadow: 0 0 10px rgba(0,0,0,.3)
  position: relative
  width: 100%
  z-index: 1
```

Now, the banner will use the $o3de-pink color instead of the original color code.


## Member Logos



## Image Updates



## Menu Changes


