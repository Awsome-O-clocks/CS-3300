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
<a href = "README.md"> Our readme </a>
```
<a href = "README.md"> Our readme </a>

If you want you can also wrap and image tag with a link, this will make it so if you click the image it will take you to a link.
Or by insead of putting a link or a path you can put an email. by you need to use the form: `mailto:email@example.com`

When you use a button you can use the onclick attribute to link to a webpage. [Learn how to do buttons.](https://www.w3schools.com/tags/tag_button.asp)


# Images

# Tables

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

# Refrences

[Elements and Tags](https://www.w3schools.com/html/html_elements.asp)

[Lists](https://www.w3schools.com/html/html_lists.asp)

[Attributes](https://www.w3schools.com/html/html_attributes.asp)