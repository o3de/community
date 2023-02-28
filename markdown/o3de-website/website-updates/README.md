# O3DE Website Updates

This is a guide to assit with common website updates for banners, color code changes, logo updates, etc. 

## Table Of Contents
  * [Banners](#banners)
  * [Color Codes](#color-codes)
  * [Member Logos](#member-logos)
  * [Image Updates](#image-updates)

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

If you want to add or remove members on the home page, make sure you have transparent logos. If you don't have transparent logos, you can use images with a background that are not too large in size.

To add a logo, place it in the `static/img/logos/partnerLogos/` folder and take note of the exact spelling and image type for later use.

Next, open the `assets/sass/custom.sass` file and scroll to line 1,000 to locate the `// layouts/partials/home/partners.html` section. To add the logo, use the following code:

```php
  .robotecai-logo
    background-image: url('/img/logos/partnerLogos/robotecai.png')
```

A few more examples on formatting:
```php
  .caict-logo
    background-image: url('/img/logos/partnerLogos/robotecai.png')
	    height: 200px
    margin: 0 -24px 0 0

  .igda-logo
    background-image: url('/img/logos/partnerLogos/robotecai.png')
    width: 120px

  .niantic-logo
    background-image: url('/img/logos/partnerLogos/robotecai.png')
    width: 128px
    margin: 0 -24px 0 0
```

Replace "robotecai" with the name of the logo you are adding, and adjust the image type as needed. If the logo is larger and does not render properly, you may need to adjust the `width`, `margin`, and `height` values.

Next, open the `layouts/partials/home/partners.html` file. Make sure there is enough room on the current slider section for the new logo. If there is not enough room, you will need to make room.

Here is an example of what the code looks like:

```html
<div class="partner-logo robotecai-logo"></div>
```

Replace "robotecai" with the name of the logo you added in the previous step. Make sure the new logo is added in the appropriate section of the file.

Adjust the `width`, `margin`, and `height` values if needed to ensure that the logo is displayed properly.

```html
<section class="home-partners pt-5 pb-5">
  <div class="container d-flex flex-column align-items-center justify-content-center">
    <h2 class="mb-3">Our Community</h2>
    <p>O3DE is built by the community in conjunction with dedicated members, including the following organizations.</p>
    <div class="row align-items-center justify-content-center partners-logos-view">

      <div id="carouselPartnersIndicators" class="carousel slide partner-carousel" data-ride="carousel" data-interval="8000">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <div class="partner-denomination">Premier Partners</div>
            <div class="partner-logo adobe-logo"></div>
            <div class="partner-logo aws-logo"></div>
            <div class="partner-logo epicgames-logo"></div>
            <div class="partner-logo huawei-logo"></div>
            <div class="partner-separator"></div>
            <div class="partner-logo intel-logo"></div>
            <div class="partner-logo lightspeedstudios-logo"></div>
            <div class="partner-logo microsoft-logo"></div>
            <div class="partner-logo niantic-logo"></div>
          </div>
          <div class="carousel-item">
            <div class="partner-denomination">Premier Partners</div>
			<div class="partner-logo oppo-logo"></div>
			<div class="partner-denomination">General Partners</div>
            <div class="partner-logo audiokinetic-logo"></div>
            <div class="partner-logo carbonated-logo"></div>
            <div class="partner-logo futurewei-logo"></div>
          </div>
          <div class="carousel-item">
            <div class="partner-denomination">General Partners</div>
            <div class="partner-logo genvid-logo"></div>
			<div class="partner-logo backtrace-logo"></div>
            <div class="partner-logo hadean-logo"></div>
            <div class="partner-separator"></div>
            <div class="partner-logo kitbash3D-logo"></div>
            <div class="partner-logo kythera-ai-logo"></div>
            <div class="partner-logo red-hat-logo"></div>
          </div>
          <div class="carousel-item">
            <div class="partner-denomination">General Partners</div>
            <div class="partner-logo side-fx-logo"></div>
			<div class="partner-logo heroic-logo"></div>
            <div class="partner-logo tafi-logo"></div>
			<div class="partner-separator"></div>
			<div class="partner-logo robotecai-logo"></div>
			<div class="partner-logo daocloud-logo"></div>
          </div>
		            <div class="carousel-item">
            <div class="partner-denomination">Associate Partners</div>
            <div class="partner-logo igda-logo"></div>
			<div class="partner-logo rit-logo"></div>
            <div class="partner-logo open-robotics-logo"></div>
			<div class="partner-separator"></div>
			<div class="partner-logo kutztown-logo"></div>
			<div class="partner-logo caict-logo"></div>
          </div>
        </div>
        <div class="d-flex justify-content-center align-items-center">
          <a data-target="#carouselPartnersIndicators" data-slide="prev" class="btn">
            <i class="fas fa-chevron-left"></i>
          </a>
          <div class="carousel-indicators mr-0 ml-0" style="position: relative">
            <a data-target="#carouselPartnersIndicators" data-slide-to="0" class="active btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
            <a data-target="#carouselPartnersIndicators" data-slide-to="1" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
            <a data-target="#carouselPartnersIndicators" data-slide-to="2" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
            <a data-target="#carouselPartnersIndicators" data-slide-to="3" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
	     <a data-target="#carouselPartnersIndicators" data-slide-to="4" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
          </div>
          <a data-target="#carouselPartnersIndicators" data-slide="next" class="btn">
            <i class="fas fa-chevron-right"></i>
          </a>
        </div>
      </div>

    </div>
  </div>
</section>
```

If we are to take this section, it would represent slider 2

```html
          <div class="carousel-item">
            <div class="partner-denomination">Premier Partners</div>
			<div class="partner-logo oppo-logo"></div>
			<div class="partner-denomination">General Partners</div>
            <div class="partner-logo audiokinetic-logo"></div>
            <div class="partner-logo carbonated-logo"></div>
            <div class="partner-logo futurewei-logo"></div>
          </div>
```
![image](https://user-images.githubusercontent.com/80487462/221715032-b75e986c-6e07-4e38-8b92-e67d5893b9fe.png)

Say we wanted to add more logos and we do not have any more room. To add another slider, you would create the following. 

```html
	            <div class="carousel-item">
          </div>
```

Followed by 

```html
	     <a data-target="#carouselPartnersIndicators" data-slide-to="5" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
```
And if we wanted to add the Logo, we would simply add

```html
			<div class="partner-logo caict-logo"></div>
```
In this case we would replace `caict-logo` with the logo name we did in the above steps

The file would then look like:

```html
.......
.......
			<div class="partner-logo robotecai-logo"></div>
			<div class="partner-logo daocloud-logo"></div>
          </div>
		            <div class="carousel-item">
            <div class="partner-denomination">Associate Partners</div>
            <div class="partner-logo igda-logo"></div>
			<div class="partner-logo rit-logo"></div>
            <div class="partner-logo open-robotics-logo"></div>
			<div class="partner-separator"></div>
			<div class="partner-logo kutztown-logo"></div>
			<div class="partner-logo caict-logo"></div>
          </div>
		            <div class="carousel-item">
			<div class="partner-logo finchy-logo"></div>
          </div>
        </div>
        <div class="d-flex justify-content-center align-items-center">
          <a data-target="#carouselPartnersIndicators" data-slide="prev" class="btn">
            <i class="fas fa-chevron-left"></i>
          </a>
          <div class="carousel-indicators mr-0 ml-0" style="position: relative">
            <a data-target="#carouselPartnersIndicators" data-slide-to="0" class="active btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
            <a data-target="#carouselPartnersIndicators" data-slide-to="1" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
            <a data-target="#carouselPartnersIndicators" data-slide-to="2" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
            <a data-target="#carouselPartnersIndicators" data-slide-to="3" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
	     <a data-target="#carouselPartnersIndicators" data-slide-to="4" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
	     <a data-target="#carouselPartnersIndicators" data-slide-to="5" class="btn carousel-btn">
              <i class="fas fa-circle"></i>
            </a>
          </div>
          <a data-target="#carouselPartnersIndicators" data-slide="next" class="btn">
            <i class="fas fa-chevron-right"></i>
          </a>
        </div>
      </div>

    </div>
  </div>
</section>
```

## Image Updates

To ensure that the website loads quickly, it's important to use images that are not too large in size. All images should be stored within the `/static/images/` folder. If you are adding images for a new event or series, I suggest creating a new folder to keep everything organized.

However, if the event happens again or the image is relevant to something else, you can keep those images in their original folder. But if the event is over and you remove the message, post, or banner associated with it, you should also remove the images to prevent stale images from cluttering the site.
