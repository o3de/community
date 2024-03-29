# O3DE Blog Cheatsheet

This is a manual that provides assistance with typical blog formatting and usage of code.

## Table Of Contents
  * [Templates and Examples](#templates-and-examples)
  * [Blog Headers](#blog-headers)
  * [Heading levels](#heading-levels)
  * [Inline elements](#inline-elements)
    + [Inline text styles](#inline-text-styles)
    + [Inline Icons](#inline-icons)
  * [Admonitions](#admonitions)
  * [Code Blocks](#code-blocks)
    + [Code blocks containing Hugo shortcodes](#code-blocks-containing-hugo-shortcodes)
  * [Links](#links)
  * [Images](#images)
  * [Embedding videos with the video shortcode](#embedding-videos-with-the-video-shortcode)
  * [Embedding Youtube videos with the youtube-width shortcode](#embedding-youtube-videos-with-the-youtube-width-shortcode)
  * [Embedding mathematical formulas in TeX and MathML](#embedding-mathematical-formulas-in-tex-and-mathml)
  * [Resources and Links](#resources-and-links)

## Templates and Examples
| Markdown  | Live Version |
| ------------- | ------------- |
| [Remote object support in Open 3D Engine](/blogs/remoteobjects)  | [Remote object support in Open 3D Engine](https://www.o3de.org/blog/posts/remote-objects/)  |
| [Vectors, Matrices & Matrix Order](/blogs/vectors-matrices-matrix-order)  | [Vectors, Matrices & Matrix Order](https://www.o3de.org/blog/posts/vectors-matrices-matrix-order/)  |


[Template](/blogs/template)
 

## Blog Headers

Blog headers are essential in every blog. This helps informs the website builder that it is in fact a blog, and tells the server how to access that page and all the top level information. 

<img width="497" alt="Image_1" src="/process-docs-and-markdown/files/media/blog-headers.PNG">

```
---
title: "CMake Essentials Series - Part 1"
date: 2022-10-05
slug: cmake-essentials-series-part-1
author: Tom Hulton-Harrop
blog_img: "/images/blog/announcement_thumbnail.jpg"
full_img: ""
---
```

`title:` Title of the blog. <br>
`date:` The date when the blog should released.  The date is NOT today's date. <br>
`slug:` Slug is the url that the blog would be visited at. For example: https://o3de.org/blog/posts/cmake-essentials-series-part-1/  <br>
`author:` Author is the person who wrote the blog. This can be First name, first and Last, or anything along those lines.  <br>
`blog_img:` Blog Image is the image that will show up in the Blog list. This will not show on the Blog itself. The default value is "/images/blog/announcement_thumbnail.jpg"  <br>
`full_img:` Full Blog image is the image that will render at the top level of the blog. This is used only when there is an image in the blog that shows at the top.  <br>

## Heading levels

The above heading is an H2. The page title renders as an H1. The following
sections show H1-H6.

```
# H1

# This is in an H1 section.

## H2

## This is in an H2 section.

### H3

### This is in an H3 section.

#### H4

#### This is in an H4 section.

##### H5

##### This is in an H5 section.

###### H6

###### This is in an H6 section.
```

<img width="374" alt="Headings" src="/process-docs-and-markdown/files/media/heading-levels.PNG">


## Inline elements

Inline elements show up within the text of paragraph, list item, admonition, or
other block-level element.

### Inline text styles

```
- **bold**
- _italic_
- ***bold italic***
- ~~strikethrough~~
- <u>underline</u>
- _<u>underline italic</u>_
- **<u>underline bold</u>**
- ***<u>underline bold italic</u>***
- `monospace text`
- **`monospace bold`**
```

<img width="150" alt="Inline" src="/process-docs-and-markdown/files/media/inline.PNG">

## Inline Icons

You can add inline O3DE GUI icons with the `icon` shortcode. Icon `.svg` files are located in `/static/images/icons`.

| Name - Image | Name - Image | Name - Image | Name - Image |
| :---: | :---: | :---: | :---: |
| <img width="186" alt="Example" src="/process-docs-and-markdown/files/media/icons1.PNG"> | <img width="188" alt="Example2" src="/process-docs-and-markdown/files/media/icons2.PNG"> | <img width="186" alt="Example3" src="/process-docs-and-markdown/files/media/icons3.PNG"> | <img width="186" alt="Example4" src="/process-docs-and-markdown/files/media/icons4.PNG"> |

## Admonitions

Admonitions (notes, warnings, etc) use Hugo shortcodes.

```
{{< note >}}
Notes catch the reader's attention without a sense of urgency.

You can have multiple paragraphs and block-level elements inside an admonition.

| Or | a | table |
| - | - | - |
| | |
{{< /note >}}
```

<img width="827" alt="Admonitions Note" src="/process-docs-and-markdown/files/media/note.PNG">

```
{{< tip >}}
Tips draw attention to a shortcut or best practice related to the preceding content.
{{< /tip >}}
```

<img width="823" alt="Admonitions Tip" src="/process-docs-and-markdown/files/media/tip.PNG">

```
{{< caution >}}
The reader should proceed with caution.
{{< /caution >}}
```

<img width="826" alt="Admonitions Caution" src="/process-docs-and-markdown/files/media/caution.PNG">

```
{{< important >}}
Important information the reader must heed.
{{< /important >}}
```

<img width="823" alt="Admonitions Important" src="/process-docs-and-markdown/files/media/important.PNG">

```
{{< todo issue="https://github.com/o3de/o3de.org/issues/432" >}}
Indicates a section needs work, followed by a description of the task and a link to the issue in GitHub.
{{< /todo >}}
```

<img width="824" alt="Admonitions To Do" src="/process-docs-and-markdown/files/media/to-do.PNG">

```
{{< known-issue >}}
Indicates a known issue with the process described in the docs. 
{{< /known-issue >}}
```

<img width="820" alt="Admonitions Known Issue" src="/process-docs-and-markdown/files/media/known-issue.PNG">

## Links

To format a link, put the link text inside square brackets, followed by the
link target in parentheses. [Link to O3DE Docs](https://www.o3de.org/docs/) or
[Relative link to O3DE.org](/)

You can also use HTML, but it is not preferred.
<a href="https://www.o3de.org">Link to O3DE.org</a>

```
To format a link, put the link text inside square brackets, followed by the
link target in parentheses. [Link to O3DE Docs](https://www.o3de.org/docs/) or
[Relative link to O3DE.org](/)

You can also use HTML, but it is not preferred.
<a href="https://www.o3de.org">Link to O3DE.org</a>
```

## Code blocks

You can create code blocks two different ways by surrounding the code block with
three back-tick characters on lines before and after the code block. **Only use
back-ticks (code fences) for code blocks.** This allows you to specify the
language of the enclosed code, which enables syntax highlighting. It is also more
predictable than using indentation.

```
this is a code block created by back-ticks
```

The back-tick method has some advantages.

- It works nearly every time.
- It is more compact when viewing the source code.
- It allows you to specify what language the code block is in, for syntax
  highlighting.
- It has a definite ending. Sometimes, the indentation method breaks with
  languages where spacing is significant, like Python or YAML.

To specify the language for the code block, put it directly after the first
grouping of back-ticks:

```bash
ls -l
```

Common languages used in O3DE documentation code blocks include:

- `bash` / `shell` (both work the same)
- `cpp`
- `python`
- `json`
- `xml`
- `none` (disables syntax highlighting for the block)

### Code blocks containing Hugo shortcodes

To show raw Hugo shortcodes as in the above example and prevent Hugo
from interpreting them, use C-style comments directly after the `<` and before
the `>` characters. The following example illustrates this (view the Markdown
source for this page).

```none
{{</* codenew file="pods/storage/gce-volume.yaml" */>}}
```

## Images

To format an image, use similar syntax to [links](#links), but add a leading `!`
character. The square brackets contain the image's alt text. Try to always use
alt text so that people using screen readers can get some benefit from the
image.

```
![O3DE icon](/img/logos/O3DE-Circle-LogoMark-REV-MONO.svg)
```

![O3DE icon](https://o3de.org/img/logos/O3DE-Circle-LogoMark-REV-MONO.svg)


The `image-width` shortcode adds an image with alternate text and restricts the image's width. The `image-width` shortcode can ensure image sizes are consistent within a topic, and that large images and `.svg` diagrams don't scale overly large in wide browser windows.

`image-width` takes three double-quoted named parameters:

1. `src="/images/<image.png>"` - Image file path.
1. `width="<image width>"` - Scale the image by specifying a width in pixels.
1. `alt="<image description>"` - A string describing the image.

`image-width` example:

```markdown
{{< image-width src="/images/welcome-guide/guide_img.png" width="700" alt="The O3DE Welcome Guide splash image." >}}
```

`image-width` example output:

![image](/process-docs-and-markdown/files/media/image-width.png)


An image can also be a link. This time the O3DE icon links to the O3DE website. Outer square brackets enclose
the entire image tag, and the link target is in the parentheses at the end.

```
[![O3DE icon](/img/logos/O3DE-Circle-LogoMark-REV-MONO.svg)](https://o3de.org)
```

[![O3DE icon](https://www.o3de.org/img/logos/O3DE-Circle-LogoMark-REV-MONO.svg)](https://o3de.org)

You can also use HTML for images, but it is not preferred.

```
<img src="/img/logos/O3DE-Circle-LogoMark-REV-MONO.svg" alt="O3DE icon" />
```

<img src="https://www.o3de.org/img/logos/O3DE-Circle-LogoMark-REV-MONO.svg" alt="O3DE icon" />



## Embedding videos with the `video` shortcode

Videos in the `/images/` directory can be embedded in topics with the `video` shortcode. Use this method to include animations in topics rather than animated `.gifs`.

Keep the following in mind when submitting videos in docs contributions:

* `.mp4` is the preferred video format. `.ogg` and `.webm` are also supported by the shortcode, but aren't as well supported by various browsers.
* Videos must be placed in the `/static/images/` directory structure using the same conventions as images.
* Videos should be smaller than 512 KB and must not exceed 1 MB in size.
* Ensure text in the video is legible if required.
* Ensure the video resolution is no larger than necessary.
* Crop and frame the subject of the video appropriately.
* Videos shouldn't include audio unless required by the example.
* Though a poster image is not required, it is recommended.

**Parameters**

`video` **requires** the following named parameters:

1. `src="/images/<video.mp4>"` - Video file path.
1. `info="<video description>"` - A string describing the video.

`video` supports the following **optional** named parameters:

1. `poster="/images/<image.png>"` - A static image that displays while the video loads or if the video fails to load. This image should be the same size and aspect ratio as the video. 
1. `autoplay="true"` - The video plays as soon as it loads.
1. `loop="true"` - The video plays in a loop.
1. `width="<video width>"` - Scale the video by specifying a width in pixels.
1. `muted="true"` - Video is muted if an audio track exists.
1. `type="video/<mp4 OR ogg OR webm>"` - Video type. MP4 is default.

The are two additional options that are always enabled.

1. `preload="auto"` - Loads the video with the page.
1. `controls` - Include player controls for the video.

**Examples**

1. Basic `video` usage with only the required parameters.

    ```markdown
      {{</* video src="/images/contributing/to-docs/TestVideo.mp4" info="This is a test video." */>}}
    ```
    Output:
    
![image](/process-docs-and-markdown/files/media/video.png)

<br>

2. Advanced `video` usage with optional parameters to enable autoplay, loop the video, scale the video to 250 pixels, and include a poster image.

    ```markdown
      {{</* video src="/images/contributing/to-docs/TestVideo.mp4" info="This is a test video." autoplay="true" loop="true" width="250" poster="/images/contributing/to-docs/TestPoster.png" */>}}
    ```

    Output:

![image](/process-docs-and-markdown/files/media/video2.png) 

Video File
https://www.o3de.org/images/contributing/to-docs/TestVideo.mp4

## Embedding Youtube videos with the `youtube-width` shortcode

Embed Youtube videos in your page by using the `youtube-width` shortcode. The `youtube-width` shortcode is an extended version of Hugo's built-in [`youtube` shortcode](https://gohugo.io/content-management/shortcodes/#youtube) that allows you to control the size of the embedded video. 

`youtube-width` supports the following double-quoted parameters:

1. id
2. title
3. width (using the default value (50%) is recommended)

**Examples** 

1. `youtube-width` example without the `width` parameter uses the default value `width: 50%`:

    ```markdown
    {{</* youtube-width id="CQmjAxr7LZs" title="What is O3DE?" */>}}
    ```

    Output:

![image](/process-docs-and-markdown/files/media/video3.png)


   <br>

2. `youtube-width` example with the `width` parameter:

    ```markdown
    {{</* youtube-width id="CQmjAxr7LZs" title="What is O3DE?" width="100%" */>}}
    ```

    Output:

![image](/process-docs-and-markdown/files/media/video4.png)


## Embedding mathematical formulas in TeX and MathML

You can embed mathematical formulas using TeX and MathML input formats, for more information on the MathJax version 3.0 display engine, please refer to the MathJax [documentation](https://docs.mathjax.org/en/latest/index.html).

**Example Usage**

```markdown
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$
```

**Example Output**

<img width="824" alt="Example" src="/process-docs-and-markdown/files/media/math.PNG">

## Resources and Links

For further learning on blog formatting, check out these links: 

- [GitHub Markdown Cheat Sheet](github-markdown.md)
- https://www.w3schools.com/html/
- https://www.markdownguide.org/extended-syntax
