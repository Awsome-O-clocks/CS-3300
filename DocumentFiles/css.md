<html>

# CSS (Cascading Style Sheets)

<!-- <style>
    body {
        font-family: "Times New Roman", Times, serif;


    }
    .Intro {
        text-align: center;
    }
    .CodeBlocks {
        background-color: #f0f0f0;
        border: 1px solid #ddd;
        border-radius: 4px;
        padding: 5px;
    }
    
</style> -->

<body>

<div class="Intro"> 

:exclamation:
CSS stands for Cascading Style Sheets. It is a stylesheet language used for describing the look and formatting of a document written in HTML (~~or in markdown, see the source code for this document :)~~ *I lied... github strips the css. :(* ). CSS describes how elements should be rendered on a device's screen.
</div>


## Function of CSS

<p>
<span style="color: skyblue;">CSS</span> is used to control the <span style="color: pink;">layout</span> and <span style="color: yellow;">appearance of HTML elements on a web page.</span> It allows you to apply styles (like colors, fonts, and spacing) and helps in creating responsive designs.
</p>

## Basic Syntax

The basic syntax of a CSS rule consists of a selector and a declaration block:

```css

.selector {
  property: value;
}
```

### Example 1: Styling a Paragraph

```css

p {
  color: blue;
}
```

### Example 2: Styling Multiple Elements

```css

h1, h2, p {
  text-align: center;
}
```

## Ways to Include CSS

### 1. Inline CSS

You can use the style attribute directly within an HTML tag.

```html

<p style="color: red;">This is a red paragraph.</p>
```


### 2. Internal CSS

You can include CSS in the HTML document within the `<style>` tags in the `<head>` section.

```html

<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
```

### 3. External CSS

You can link to an external CSS file using the `<link>` tag.

```html

<head>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
```

## In styles.css:

```css

p {
  color: green;
}
```

## Common CSS Properties

Here are some commonly used CSS properties:
```css

color: /* Sets the text color */
font-size: /* Sets the font size */
margin: /* Sets the margin around elements */
padding: /* Sets the padding inside elements */
border: /* Sets the border around elements */
```

</body>
</html>