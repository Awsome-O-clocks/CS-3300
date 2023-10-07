# HTML Sheets

## Tabel of Contents
- [Elements](#elements)
- [Lists](#lists)
  - [Quick Summary](#quick-summary) 
- [Links](#links)
- [Images](#images)
- [Tables](#Tables)
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

# Images

# Tables

# Comments

# Refrences

[Elements and Tags](https://www.w3schools.com/html/html_elements.asp)

[Lists](https://www.w3schools.com/html/html_lists.asp)