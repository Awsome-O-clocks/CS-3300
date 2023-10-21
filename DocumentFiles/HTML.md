# HTML Sheets

## Tabel of Contents
- [Elements](#elements)
- [Lists](#lists)
  - [Quick Summary](#quick-summary) 
- [Links](#links)
- [Images](#images)
- [Tables](#Tables)
- [Attributes](#attributes)
- [Comments](#Comments)
- [Refrences](#Refrences)


# Elements

Everything inclusively from tag to tag
```
<Tag> Content </Tag>
```

## Tags

Most Tags use a starter and ender tag

- `h1 Ex: <h1> Biggest heading size </h1> ` 
- `p Ex: <p> Paragraph text </p> `
- `body Ex: <body><p> Paragraph text </p></body>`
- `html Ex: <html> <body> <p>All content on a page is put inside a html tag.</p> <body> <\html>`

Not all tags need a ending 
- `br <p>This line starts the paragraph. <br> This will be on the next line.<\p>`

As you can see you can also nest tags inside of each other. You can also use the lower case or upercase version of these, your prefrence.

> :warning: 
> if you forget the end tag you will have problems its just like forgetting a parenthiese or a semicolon  

# Lists

There are two main types of lists; there are ordered lists and unored lists.
 
 Orderd
 1) item
 2) item
 3) item

 Unorderd
 * item
 * item
 * item

 ## List Tags
First thing to understand is that `li Ex: <li>Is essentially a row in a list</li>`

`ol` is the basic name of <u><b>O</b></u>rderd lists
```
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>

If you look at this page's code you will see I made this list with html, and also take a look at the bolded and underlined O.

`ul` is the basic name of <u><b>U</b></u>norderd lists

```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>

I encourage you to look at the code for how I made the [Table of Contents](#tabel-of-contents). Please note that it is written in Markdown, not HTML. Now, look at the code for [these lists](#lists); they don't use tags either. HTML is very different. It uses tags to indicate what text is supposed to be doing, while Markdown uses much simpler methods. You might think to yourself, 'Why doesn't everyone use Markdown formatting? It's SO MUCH SIMPLER!!!' Well, why don't people use Python for everything? Because Python is slow but easy to use. HTML is very standardized and is meant to help display web pages. Not to mention, Markdown is using HTML; it's just hidden behind the scenes. Ever use LaTeX its disguised HTML. So, it's important to learn HTML if you ever plan on interacting with any kind of text editor for the web. Besides, it's easy, like C, it can be nitpicky, but once you understand it, you'll be best friends.

There are also descriptive lists I bet you can't guess the tag :) `dl`

```
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>

Take a second look at that code, WAH!! It doesnt use `<li>`?

`dt` defines the term or the name.
`dd` defines the definition. 

You can remember these with <u><b>D</b></u>escriptive <u><b>T</b></u>erm, and <u><b>D</b></u>escriptive <u><b>D</b></u>efinition.

## Quick Summary

`ul` unordered list

`ol` ordered list

`li` list item

`dl` descriptive list

`dt` descriptive term

`dd` descriptive definition

# Links

Links allow you to jump to other pages. In HTML a link uses 

`a Ex: <a href='url'>Link text</a>`

Href is your first refrence to an attribute. [Learn more](#attributes)

### Links have a few important attributes:

The target attribute defines how and where to a link, and can take a few velues to help specify that.

`_self` is the default and opens a link in the same tab as it was clicked. The `_blank` value opens the link in a seperate tab. `_parent` opens the document in the parent frame. `_top` opens the document in the full body of the window.

Title is used to specify a more information about a link. 
<a href="README.md" title="Go to out README page">Try hovering over me!</a>

### Different types of paths

Absolute paths will take you outside the scope of your project to find a file.
Heres an example

```
<a href = "https://github.com/Awsome-O-clocks/CS-3300/blob/main/README.md"> Our readme </a>
```
<a href = "https://github.com/Awsome-O-clocks/CS-3300/blob/main/README.md"> Our readme </a>

Releative paths seach with in the files of your page or project

```
<a href = "../README.md"> Our readme </a>
```
<a href = "../README.md"> Our readme </a>

If you want you can also wrap and image tag with a link, this will make it so if you click the image it will take you to a link.
Or by insead of putting a link or a path you can put an email. by you need to use the form: `mailto:email@example.com`

When you use a button you can use the onclick attribute to link to a webpage. [Learn how to do buttons.](https://www.w3schools.com/tags/tag_button.asp)


# Images

So you wanna put some pretty pictures on to your webpage. Well then lets dive right in to something that seems simple.

Here's the tag:

`img Ex: <img src="PrettyPictre.img" alt="A van gogh sunflower painting">`

Just want to bring your attention to the alt here for a second, by using the alternate text here I can describe to you what this image is whithout showing you the image. Screen readers use the alternate text to decribe to low vision web users the image.\

Style attribute id used to set the width and hight of your image. Use this format:
`style="width:500px;height:600px"`

If you don't want to use style use this format:
`width="500" height="600"`
In this case the with and heights are attributes in the previous example they were values.

### Image floating

That was easy <img src=".\images\That_was_easy.jpg" alt="That was easy meme" height="25%" width="25%">

Well thats not a pretty formatting for that image... but I resized it i put i on the right line. Help...

<img src=".\images\That_was_easy.jpg" alt="That was easy meme" height="25%" width="25%" style="float:left">


Well this is a better format, the text is at the top of the page, and I can write what I want over here. But how?


The float method alows you to put a page basicly any where you want here I used `float:left` so that the image is on the left and the words are on the right.

But remember this floating can cause a lot of issues if your not careful. For exampe when I put the image in and asked it to float left suddently Tables and attribues headings were overlapping my image. Images can be dificult and not like the image says at all.

But don't give up, every single webpage uses them so they arn't imposible.


# Tables

Tables can be unintuitve but im here to help we've got this!!!

First the starter tag is super simple its just `table`. Next, each row has a tag `tr` or <u><b>t</b></u>able <u><b>r</b></u>ow. Next the colums these have actualy 2 differnt tags but their easy too. If your writting the title of the column use `th` for <u><b>t</b></u>able <u><b>r</b></u>ow and if your wriing a standard data in the column use `td` for <u><b>t</b></u>able <u><b>d</b></u>ata. Easy!!!

Here's some example code: you'll notice that it may not be what you expected, but if you look at it as each row has multiple colums and the first 3 are the headers it might make more since.

```
<table>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>
```
<table>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>

Notice the headers are bolded.

You can also move those to the side if you want to make a horizontal table, takes a bit of reconfiguring but if you stay focused its easy.

```
<table>
  <tr>
    <th>Company</th>
    <td>Alfreds Futterkiste</td>
    <td>Centro comercial Moctezuma</td>
  </tr>
  <tr>
    <th>Contact</th>
    <td>Maria Anders</td>
    <td>Francisco Chang</td>
  </tr>
  <tr>
    <th>Country</th>
    <td>Germany</td>
    <td>Mexico</td>
  </tr>
</table>
```
<table>
  <tr>
    <th>Company</th>
    <td>Alfreds Futterkiste</td>
    <td>Centro comercial Moctezuma</td>
  </tr>
  <tr>
    <th>Contact</th>
    <td>Maria Anders</td>
    <td>Francisco Chang</td>
  </tr>
  <tr>
    <th>Country</th>
    <td>Germany</td>
    <td>Mexico</td>
  </tr>
</table>

Take a look and make sure you understand what I changed around.

# Attributes

All HTML attributes have attributes, they provide additional information about elements. Attributes are only ever defined in the start tag.

Its important to understand what attributes are availiable to you for each tag. 

Just a few examples include:

* Alt, provides a way to put allternate text for images. 
* href, provides a link/path
* src, provides an image path
* style, allows controll over color font size and more.
* lang, is used to specify the language of a page.

There are quite a few attributes you need to keep in mind to make your webpage more accesiable. Do your research to find out how you can make your page more accesible. Screen readers use alot of information in your html to help people read. Remember to use them any time you can.

Remember one of the easiest things to make you webpage more accessible is to use alt text in images. Markdown's alternate text is inside the brackets so remember to make whats inside the brackets is important don't just put `![Image](image/path)` put `![image of diagram, titled: title, describe the image](image/path)` It doesn't need to be a perfect description but if you can draw the imporant element based on the description its good.

[Accsessiblilty W3 schools](https://www.w3schools.com/html/html_accessibility.asp)

[Web Accessibility intiative](https://www.w3.org/WAI/standards-guidelines/)

[Accessibility for people with cognitive and learning disabilities](https://www.w3.org/WAI/cognitive/)


# Comments

Comments are exaxtly what they sound like. A way to communicate inside of the code and make sure developers understand what your code does, how to use it, and if there is anything that might not be working as expected warn people about it so its not forgotten and fixed.

Format:

```
<!-- Comment here -->
```

This is the same format as a multiline comment and can even be used inside code and it doesnt have to be outside or at the end of a section of code.

# Forms

<form>
<input type="text"><br>
<input type="radio"> These must have an name attribute to link multiple together<br> 
<input type="checkbox">These must have an name attribute to link multiple together<br>
<input type="submit"><br>
<input type="button"><br>
</form>

<form>
<label for = "tempRadio1"> option 1 </label>
<input type="radio" name = “TempRadio” id="TempRadio1"><br>
<input type="radio" name = “TempRadio” id="TempRadio2">
<label for = "tempRadio2"> option 2 </label><br>
<input type="radio" name = “TempRadio” id="TempRadio3"> 
<p>option 3</p>
</form>



# Refrences

[Elements and Tags](https://www.w3schools.com/html/html_elements.asp)

[Lists](https://www.w3schools.com/html/html_lists.asp)

[Attributes](https://www.w3schools.com/html/html_attributes.asp)

[Images](https://www.w3schools.com/html/html_images.asp)

[Tabels](https://www.w3schools.com/html/html_tables.asp)

[Comments](https://www.w3schools.com/html/html_comments.asp)

[Forms](https://www.w3schools.com/html/html_forms.asp)