# O3DE Blog Cheatsheet

This is a guide to assit with common blog formatting and code uses. 

## Table Of Contents
  * [Templates and Examples](#templates-and-examples)
  * [Blog Headers](#blog-headers)
  * [Heading levels](#heading-levels)
  * [Inline elements](#inline-elements)
    + [Inline text styles](#inline-text-styles)
    + [Inline Iconss](#ineline-icons)
  * [Admonitions](#admonitions)
  * [Embedding mathematical formulas in TeX and MathML](#embedding-mathematical-formulas-in-teX-and-mathml)
  * [Resources and Links](#resources-and-links)

# O3DE-Website

Here's a guide community members can use to help create blog content. 

## Templates and Examples
remoteobjects
| Markdown  | Live Version |
| ------------- | ------------- |
| [Remote object support in Open 3D Engine](/blogs/remoteobjects)  | [Remote object support in Open 3D Engine](https://www.o3de.org/blog/posts/remote-objects/)  |
| [Vectors, Matrices & Matrix Order](/blogs/vectors-matrices-matrix-order)  | [Vectors, Matrices & Matrix Order](https://www.o3de.org/blog/posts/vectors-matrices-matrix-order/)  |


[Template](/blogs/template)
 

## Blog Headers

Blog headers are essential in every blog. This helps show the website that it is infact a blog, and tells the server how to access that page, and all the top level information. 

<img width="497" alt="Image_1" src="https://user-images.githubusercontent.com/80487462/216458705-b25f96df-6722-441e-8a05-3193afc7c260.PNG">

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
`date:` Date would be the date of the blog being released.  The date is NOT todays dates. <br>
`slug:` Slug is the url that the blog would be visited at. For example: https://o3de.org/blog/posts/cmake-essentials-series-part-1/  <br>
`author:` Author is the person who wrote the blog. This can be First name, first and Last, or anything along those lines.  <br>
`blog_img:` Blog Image is the image that will show up in the Blog list. This will not show on the Blog it's self. The default value is "/images/blog/announcement_thumbnail.jpg"  <br>
`full_img:` Full Blog image is the image that will render at the top level of the blog. This is used only when there is a image in the blog that shows at the top.  <br>

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

<img width="374" alt="Headings" src="https://user-images.githubusercontent.com/80487462/220471084-3cfeb84c-7821-4eea-a710-edcdd59e5b95.PNG">


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

<img width="150" alt="Inline" src="https://user-images.githubusercontent.com/80487462/220466082-1a4cbb09-c3c1-4460-bab9-e4ca4f8ae32b.PNG">

## Inline Icons

You can add inline O3DE GUI icons with the `icon` shortcode. Icon `.svg` files are located in `/static/images/icons`.

| Name - Image | Name - Image | Name - Image | Name - Image |
| :---: | :---: | :---: | :---: |
| <img width="186" alt="Example" src="https://user-images.githubusercontent.com/80487462/220469734-de8efa54-eaaf-43f5-a7f8-f338edcad7f3.PNG"> | <img width="188" alt="Example2" src="https://user-images.githubusercontent.com/80487462/220469792-bb7a163a-5a65-4f36-a7be-3e68a2275b98.PNG"> | <img width="186" alt="Example3" src="https://user-images.githubusercontent.com/80487462/220469835-6168a599-0fb3-4483-8bea-2b57ac7e5452.PNG"> | <img width="186" alt="Example4" src="https://user-images.githubusercontent.com/80487462/220469861-34a43fcb-0ea3-4f17-8d45-cd68547ffa6f.PNG"> |

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

<img width="827" alt="Admonitions Note" src="https://user-images.githubusercontent.com/80487462/220466605-88f00ecb-6aa9-4cbf-bb4c-f52981b5546b.PNG">

```
{{< tip >}}
Tips draw attention to a shortcut or best practice related to the preceding content.
{{< /tip >}}
```

<img width="823" alt="Admonitions Tip" src="https://user-images.githubusercontent.com/80487462/220466741-5addf01f-27b9-4115-84ac-f9537b30a205.PNG">

```
{{< caution >}}
The reader should proceed with caution.
{{< /caution >}}
```

<img width="826" alt="Admonitions Caution" src="https://user-images.githubusercontent.com/80487462/220466819-cc65e88a-3391-4742-a48e-8c3ab54423fa.PNG">

```
{{< important >}}
Important information the reader must heed.
{{< /important >}}
```

<img width="823" alt="Admonitions Important" src="https://user-images.githubusercontent.com/80487462/220466980-93fadb82-b40d-40d5-8116-8064a39b097f.PNG">

```
{{< todo issue="https://github.com/o3de/o3de.org/issues/432" >}}
Indicates a section needs work, followed by a description of the task and a link to the issue in GitHub.
{{< /todo >}}
```

<img width="824" alt="Admonitions To Do" src="https://user-images.githubusercontent.com/80487462/220466902-674f83b9-94b4-4624-9cb4-ee7510b0d471.PNG">

```
{{< known-issue >}}
Indicates a known issue with the process described in the docs. 
{{< /known-issue >}}
```

<img width="820" alt="Admonitions Known Issue" src="https://user-images.githubusercontent.com/80487462/220467125-61ea902a-d96d-4734-96f1-e845065840e8.PNG">

## Embedding mathematical formulas in TeX and MathML

You can embed mathematical formulas using TeX and MathML input formats, for more information on the MathJax version 3.0 display engine, please refer to the MathJax [documentation](https://docs.mathjax.org/en/latest/index.html).

**Example Usage**

```markdown
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$
```

**Example Output**

<img width="824" alt="Example" src="https://user-images.githubusercontent.com/80487462/220468038-58402a20-23c2-4bc0-a41f-314d33157709.PNG">

## Resources and Links

For further learning on blog formatting, check out these links: 

https://www.w3schools.com/html/
