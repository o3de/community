# Github Markdown Cheat Sheet

This guide is sure to assist with anyone who is looking to update their `.readme` files or create new repositories. If there are any updates, changes or alterations needed, please be sure to submit an issue or pr to get it resolved.

## Table Of Contents
  * [Headers](#headers)
  * [Emphasis](#emphasis)
  * [Lists](#lists)
    + [Unordered](#unordered)
    + [Ordered](#ordered)
  * [Images](#images)
  * [Links](#links)
  * [Blockquotes](#blockquotes)
  * [Horizontal Rules](#horizontal-rules)
  * [Tabels](#tabels)
  * [Blackslash escape](#blackslash-escape)
  * [Task Lists](#task-lists)
  * [Inline HTML](#inline-html)
  * [Colapsable section](#colapsable-section)
  * [Link to the top of the page or a specific section on said page](#link-to-the-top-of-the-page-or-a-specific-section-on-said-page)
  * [Fenced Code Blocks](#fenced-code-blocks)
  * [Syntax highlighting](#syntax-highlighting)
    + [No highlighting](#no-highlighting)
    + [Highlighting](#highlighting)
    + [JavaScript Syntax](#javascript-syntax)
    + [Python Syntax](#python-syntax)
    + [HTML Syntax](#html-syntax)
    + [No Langauage](#no-langauage)
  * [Inline code](#inline-code)
  * [Emoji](#emoji)
  * [Username @ mentions](#username--mentions)
  * [Issue References](#issue-references)
  * [Hotkey](#hotkey)
  * [Footnotes](#footnotes)
  * [YouTube Videos](#youtube-videos)

```
## Table Of Contents
  * [Headers](#headers)
  * [Emphasis](#emphasis)
  * [Lists](#lists)
    + [Unordered](#unordered)
    + [Ordered](#ordered)
  * [Images](#images)
  * [Links](#links)
  * [Blockquotes](#blockquotes)
  * [Horizontal Rules](#horizontal-rules)
  * [Tabels](#tabels)
  * [Blackslash escape](#blackslash-escape)
  * [Task Lists](#task-lists)
  * [Inline HTML](#inline-html)
  * [Colapsable section](#colapsable-section)
  * [Link to the top of the page or a specific section on said page](#link-to-the-top-of-the-page-or-a-specific-section-on-said-page)
  * [Fenced Code Blocks](#fenced-code-blocks)
  * [Syntax highlighting](#syntax-highlighting)
    + [No highlighting](#no-highlighting)
    + [Highlighting](#highlighting)
    + [JavaScript Syntax](#javascript-syntax)
    + [Python Syntax](#python-syntax)
    + [HTML Syntax](#html-syntax)
    + [No Langauage](#no-langauage)
  * [Inline code](#inline-code)
  * [Emoji](#emoji)
  * [Username `@` mentions](#username-----mentions)
  * [Issue References](#issue-references)
  * [Hotkey](#hotkey)
  * [Footnotes](#footnotes)
  * [YouTube Videos](#youtube-videos)
```


## Headers 

```markdown
# This is an <h1> tag
  
## This is an <h2> tag 

### This is an <h3> tag   
  
#### This is an <h4> tag 
  
##### This is an <h5> tag
  
###### This is an <h6> tag
```

# This is an \<h1\> tag
  
## This is an \<h2\> tag 

### This is an \<h3\> tag   
  
#### This is an \<h4\> tag 
  
##### This is an \<h5\> tag
  
###### This is an \<h6\> tag
  
## Emphasis

```markdown
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

~~This text will be crossed out (strikethrough)~~ 

_You **can** combine them_

***All this text is bold and italic***
```

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

~~This text will be crossed out (strikethrough)~~ 

_You __can__ combine them_

***All this text is bold and italic***

## Lists

### Unordered

```markdown
* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

* Item 1
* Item 2
  * Item 2a
  * Item 2b

### Ordered

```markdown
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b

## Images 

*Note: When linking images, it is advised to create a folder in the `.readme`'s location named "Media" or "Images" to place to image in. Attaching media by other methods such as dragging & dropping or pasting may only provide a temporary link to the image in GitHub's cache.* 

If you are maintaining a repository that uses LFS (Large File Support), then you may encounter issues uploading and displaying images. If so, you may need to modify the repository on the host end (GitHub) to allow uploading of these images:

Navigate to the `.gitattributes` file in the repository. Search for the files that you are using in the `.readme` (Usually it will be `.png`). It should look something like this:

`*.png filter=lfs diff=lfs merge=lfs -text`

Copy and paste at the bottom of the text file including the file those images are stored in, for example:

`Media/*.png filter= diff= merge= -text`
or
`Images/*.png filter= diff= merge= -text`


```markdown
Format:  ![Alt Text](url)
Example: ![Newspaper Delivery Game](https://github.com/o3de/NewspaperDeliveryGame/blob/main/Media/image7.png)
```

If the image is in the same directory as this readme, you would use the following:

```markdown
Format:  ![Alt Text](url)
Example: ![Newspaper Delivery Game](/Media/image01.png)
If "Media" is where your images are located. 
```

![Newspaper Delivery Game](https://github.com/o3de/NewspaperDeliveryGame/blob/main/Media/image7.png)

## Links 

```markdown
http://github.com - automatic!
```

http://github.com - automatic!

```markdown
Format:  [Test](url)
Example: [GitHub](http://github.com)
```

[GitHub](http://github.com)

## Blockquotes

```markdown
As Bruce Banner said:

> That’s my secret, Captain.
> I’m always angry.
```

As Bruce Banner said:

> That’s my secret, Captain.
> I’m always angry.

Blockquotes can be nested.

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

## Horizontal Rules

Horizontal rules can be created using three or more asterisks (\*\*\*), dashes (\-\-\-), or underscores (\_\_\_) on a line by themselves.

```markdown 
*** 
----
______
```

*** 
----
______

## Tables 

```markdown
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

```markdown
| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
```

| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |

Your Markdown does't have to be pretty. 

There must be at least 3 dashes separating each header cell. The outer pipes (`|`) are optional, and you don't need to make the table columns line up perfect.

```markdown
Less | Pretty | Markdown 
--- | --- | ---
1 | 2 | 3 
*Still* | `renders` | **as expected**
4 | 5 | 6
```

Less | Pretty | Markdown 
--- | --- | ---
1 | 2 | 3 
*Still* | `renders` | **as expected**
4 | 5 | 6

## Blackslash escape

Markdown allows you to use backslash escapes to generate literal characters which would otherwise have special meaning in Markdown’s formatting syntax.

| Name                  | Markdown  | Result |
| --------------------- | --------- | ------ |
| backslash             | `\\`      | \\     |
| backtick              | `` \` ``  | \`     |
| asterisk              | `\*`      | \*     |
| underscore            | `\_`      | \_     |
| curly braces          | `\{\}`    | \{\}   |
| square brackets       | `\[\]`    | \[ \]  |
| parentheses           | `\(\)`    | \(\)   |
| hash mark             | `\#`      | \#     |
| plus sign             | `\+`      | \+     |
| minus sign (hyphen)   | `\-`      | \-     |
| dot                   | `\.`      | \.     |
| exclamation mark      | `\!`      | \!     |

## Task Lists

```
- [x] this is a complete item 
- [ ] this is an incomplete it
   - [ ] A subtask
```

- [x] this is a complete item 
- [ ] this is an incomplete it
   - [ ] A subtask

## Inline HTML

Markdown also supports raw HTML.

```html
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>
```

<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>

```html
<p>Markdown in HTML does *not* work **well**. Use <i>HTML</i> <b>tags</b> instead.</p>
```

<p>Markdown in HTML does *not* work **well**. Use <i>HTML</i> <b>tags</b> instead.</p>

## Collapsible section


<details>
  <summary>Title 1</summary>
  <p>Content 1 Content 1 Content 1 Content 1 Content 1</p>
</details>
<details>
  <summary>Title 2</summary>
  <p>Content 2 Content 2 Content 2 Content 2 Content 2</p>
</details>


```markdown
<details>
 <summary>Title 1</summary>
 <p>Content 1 Content 1 Content 1 Content 1 Content 1</p>
</details>
```  

## Link to the top of the page or a specific section on said page

[Go To TOP](#table-of-contents)
<a name="table-of-contents"></a>
   
```markdown
[Go To TOP](#table-of-contents)
<a name="table-of-contents"></a>
``` 

```markdown
[a Name](#Section-ID)
<a name="Section-ID></a>
```   
  

## Fenced Code Blocks

You can create fenced code blocks by placing triple backticks ` ``` ` before and after the code block. Place a blank line before and after code blocks to make the raw formatting easier to read.

```
function test() {
  console.log("notice the blank line before this function?");
}
```

To display triple backticks in a fenced code block, wrap them inside quadruple backticks.

````````
````
```
Look! You can see my backticks.
```
````
````````

````
```
Look! You can see my backticks.
```
````

## Syntax highlighting

You can add an optional language identifier to enable syntax highlighting in your fenced code block.

For example, to syntax highlight Ruby code:

````
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
````

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

### No highlighting 

````markdown
```
if (isAwesome){
  return true
}
```
````

```
if (isAwesome) {
  return true
}
```

````
```markdown
var s = "JavaScript syntax highlighting";
alert(s);
```
````

```markdown
var s = "JavaScript syntax highlighting";
alert(s);
```

### Highlighting 

````markdown
```javascript 
if (isAwesome){
  return true
}
```
````

```javascript
if (isAwesome) {
  return true
}
```

### JavaScript Syntax

````
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
````

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
### Python Syntax

````
```python
s = "Python syntax highlighting"
print s
```
````

```python
s = "Python syntax highlighting"
print s
```

### HTML Syntax
````
``` html
<p><pre><code class="language-html">&lt;p&gt;HTML Document&lt;/p&gt;
</code></pre></p>
```
````

``` html
<p><pre><code class="language-html">&lt;p&gt;HTML Document&lt;/p&gt;
</code></pre></p>
```
 
### No Langauage

````
```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```
````

```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

You can have list/line code sections as well. 

````
Title
----
- Line1
  ```bash
  ls
  ```
  - Line2
    ```bash
    ls -l
    ```
````

#### Title
----
- Line1
  ```bash
  ls
  ```
  - Line2
    ```bash
    ls -l
    ```

## Inline code

```markdown
I think you should use an `<addr>` element here instead.
```

I think you should use an `<addr>` element here instead.

## Emoji

Look up emoji codes at [emoji-cheat-sheet.com](http://emoji-cheat-sheet.com/)

```markdown
:+1: :sparkles: :camel: :tada: :rocket: :metal:
```

:+1: :sparkles: :camel: :tada: :rocket: :metal:

## Username @ mentions
Typing an @ symbol, followed by a username, will
notify that person to come and view the comment.
This is called an “@mention”, because you’re
mentioning the individual. You can also @mention
teams within an organization.

## Issue References
Any number that refers to an Issue or Pull Request
will be automatically converted into a link. Note this issue has to be located from within the repository that you are doing your work in. 
#1


## Hotkey

<kbd>⌘F</kbd>

<kbd>⇧⌘F</kbd>

```markdown
<kbd>⌘F</kbd>
``` 

Hotkey list:

| Key | Symbol |
| --- | --- |
| Option | ⌥ |
| Control | ⌃ |
| Command | ⌘ |
| Shift | ⇧ |
| Caps Lock | ⇪ |
| Tab | ⇥ |
| Esc | ⎋ |
| Power | ⌽ |
| Return | ↩ |
| Delete | ⌫ |
| Up | ↑ |
| Down | ↓ |
| Left | ← |
| Right | → |


## Footnotes

Footnotes aren't part of the core Markdown spec, but they are supported on GitHub.

```Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.
```

Reners to: 

![footnote](/process-docs-and-markdown/files/media/footer.png)


## YouTube Videos

Youtube videos can't be embedded directly but you can add an image with a link to the video like this:

```markdown
<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>
```

<a href="http://www.youtube.com/watch?feature=player_embedded&v=YOUTUBE_VIDEO_ID_HERE
" target="_blank"><img src="http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>

Or, in pure Markdown, but without the image sizing and border:

```markdown
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)
```

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

