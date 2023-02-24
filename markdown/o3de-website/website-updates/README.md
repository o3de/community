# O3DE Website Updates

This is a guide to assit with common website updates for banners, color code changes, logo updates, etc. 

## Table Of Contents
  * [Banners](#banners)
  * [Color Codes](#color-codes)
  * [Member Logos](#member-logos)
  * [Image Updates](#image-updates)
  * [Menu Changes](#menu-changes)

## Banners

When you want to add banners, you can find an existing banner in the backend that can be enabled and edited. This banner was created for the O3DCon 2022, and you can find the pull request at https://github.com/o3de/o3de.org/pull/1764.

To activate the banner on any page, simply add `{{ partial "top-banner.html" . }}` to the pages where you want it to appear:

   `/layouts/download/section.html` - Top of Download Page
   `/layouts/contribute/section.html` - Top of Contribute Page
   `/layouts/community/section.html` - Top of Community Page
   `/layouts/index.html` - Top of Home/Index Page

To add `{{ partial "top-banner.html" . }}`, you would need to add it to the code like this:

```php
{{ define "main" }}
{{ partial "top-banner.html" . }}
{{ partial "community/hero.html" . }}
{{ partial "community/join.html" . }}
<div class="community-blog d-flex align-items-center text-light">
```

The banner can be found and edited in `layouts/partials/top-banner.html`

```html
<a class="top-banner" href="https://events.linuxfoundation.org/o3decon/" target="_blank">
  <div class="top-notification">
    <div class="banner-logo"></div>
    <div class="banner-title">
	<span class="mobile-only">O3DCON: October 18 – 19, 2022 <br> Workshop Day: October 17</span>
	<span class="desktop-only">October 18 – 19, 2022 / Workshop Day: October 17</span>
	</div>
    <div class="banner-subtitle">Austin, Texas
    </div>
    <div class="banner-call-to-action">REGISTER</div>
  </div>
</a> 
```

Will render:
![image](https://user-images.githubusercontent.com/80487462/221308859-e9765572-1cc0-406a-9575-f1b37dacee12.png)

To edit the colors, these can be accessed in `assets/sass/custom.sass`


## Color Codes

To incorporate a new color to the website, the existing colors can be found in the website folder under `assets/sass` in the `custom.sass` file. The color codes are available around line 70 in a section. This section makes it easier to reference the color code instead of looking up the Hex code.

To add a new color, insert a new line under the `// Variables` section. For example:

If the existing section looks like this:

```php
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

```php
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

```php
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

To ensure that the website loads quickly, it's important to use images that are not too large in size. All images should be stored within the `/static/images/` folder. If you are adding images for a new event or series, I suggest creating a new folder to keep everything organized.

However, if the event happens again or the image is relevant to something else, you can keep those images in their original folder. But if the event is over and you remove the message, post, or banner associated with it, you should also remove the images to prevent stale images from cluttering the site.

## Menu Changes


