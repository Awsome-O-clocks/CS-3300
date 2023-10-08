## General Information

Bootstrap is a free front-end framework for quick and easy we development. This framework includes **HTML** and **CSS** based templates. These are a range of templates from typography, forms, buttons, tables, navigation, modals, image carousels, and others. These can also include **JavaScript** plugin. These builds gives the ability to easily create responsive designs.

***RESPONSIVE DESIGN***: Is the ability to have the web site automatically adjust themselves to look good on all devices, from phones to desktops.

>:warning: Boostrap 5 switched to **JavaScript** instead of the predicesors that used **jQuery**, Boostrap 3 and 4 are still supported but will not have the newer features from 5.

***

## Downloading Bootstrap

To get first download it from [Getbootstrap](https://github.com/twbs/bootstrap/releases/download/v5.3.2/bootstrap-5.3.2-dist.zip) or can compile from [Source](https://github.com/twbs/bootstrap/archive/v5.3.2.zip)

### Django Method (Package Manager Method)

To do this for ***Django*** do the following:

in Linux:
```
Scripts\activate.bat
```

Windows:
```
Scripts\activate.ps1
```

once in the *venv* run the following to install Bootstrap5:
```
pip install django-bootstrap-v5
```
The output should show the following:
![1a17d93a74b53e3158e46b6467b8f4f7.png](../_resources/1a17d93a74b53e3158e46b6467b8f4f7.png)

In the `settings.py` configuration file under the `INSTALLED_APPS` add `bootstrap5,` at the end of the file should look something like this.
```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'portfolio',
    'bootstrap5',
]
```


### Alternative Method

If not wanting to download and host Bootstrap, can include it from a **Content Delivery Network (CDN)** 
[CDN info from cloudflare](https://www.cloudflare.com/learning/cdn/what-is-a-cdn/) 

The baseline recommendation for CDN is ***jsDelivr***. The direct Libraries are found [here](https://cdnjs.com/libraries/bootstrap), It is highly recommended to use *jsDelivr*.

:memo: An advantage of using Bootstrap CDN is that it is cached from other sites so wit will reload the cache from the past sites that were given **increasing load times**. Additionally, boostrap uses jQuery for the JavaScript plugins, these and jQuery are not needed if only wanting to use the ***CSS*** portions of Boostrap.

```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
```

To perform separate downloads with packages using bootstrap's compiled JavaScript do the following to add **Popper** before the JS.
```
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.min.js" integrity="sha384-BBtl+eGJRgqQAUMxJ7pMwbEyER4l1g+O15P+16Ep7Q9Q+zqX6gSbd85u4mG4QzX+" crossorigin="anonymous"></script>
```
>:warning: Make sure to check the SHA384 hash or **SRI** hash of a given file to ensure that it hasn't been modified by anyone. To do this you can do it through your own system or use the following tool to check [SRI HASH GENERATOR](https://www.srihash.org/). 

Another method of pulling in the Bootstraps source files is through package managers. This still requires two components a [Sass complier](https://getbootstrap.com/docs/5.3/getting-started/contribute/#sass) and [Autoprefixer](https://github.com/postcss/autoprefixer) that matches the Bootstrap's compiled versions.

***

## Building Pages With Bootstrap

Bootstrap uses ***HTML5*** doctype, so this must always be present at the beginning of page.
:warning: This is a global that is required for Boostrap
```html
<!doctype html>
<html lang="en">
  ...
</html>
```

### Django Method:

```html
<!DOCTYPE html>
<html>
<head>
  <title>{% block title %}{% endblock %}</title>
  {% load bootstrap5 %}
  {% bootstrap_css %}
  {% bootstrap_javascript %}
</head>
<body>

<div class="container">
  <ul class="nav bg-info">
    <li class="nav-item">
      <a class="nav-link link-light" href="/">HOME</a>
    </li>
    <li class="nav-item">
      <a class="nav-link link-light" href="/login">Login</a>
    </li>
  </ul>

  {% block content %}
  {% endblock %}
</div>
</body>
</html>

```

```html
{% load bootstrap5 %}
{% bootstrap_css %}
{% bootstrap_javascript %}
```

- The above is telling Django and HTML to load bootstrap5.
- The second line inserts the `<link>` element with the referral to the bootstrap stylesheet.
- The third line inserts the `<script>` element with the referral to the necessary javascript file.

### EXAMPLE:

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Bootstrap demo</title>
	<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
	</head>
	<body>
		<h1>HEADERS ARE ALWAYS THERE</h1>
		<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
	</body>
</html>
```

The `meta name='viewport'` tag is what builds the responsive behavior **THIS IS REQUIRED FOR OPTIMIZATION**, this is a method of using the CDN linking in the scripting language denoted by the `link href=`. To save memory and space if not wanting to utilize the dropdowns, popovers, or tooltips, etc utilize the second method of the CDN that was described earlier.

- For More mobile configurations go [here](https://getbootstrap.com/docs/5.3/getting-started/browsers-devices/)

Looking at the `cdn.jsdelivr.net/npm/` portion notice the `/dist/` are different these have `css` and `js` one is pulling the CSS and one is pulling the JavaScript portions. To get other builds the following are [listed](https://getbootstrap.com/docs/5.3/getting-started/contents/).

## Important Notes and links

:warning: Bootstrap5 dropped support for Internet Explorer

[**Testing code**](https://codepen.io/team/bootstrap/pen/qBamdLj): Link to test some of the features if wanting to try to implement.
[**Reboot**](https://getbootstrap.com/docs/5.3/content/reboot/) : Is an element-specific CSS changes in a single file, this is where content customization is built.
[**Themes and Extended Boostrap with Saas**](https://getbootstrap.com/docs/5.3/customize/overview/): 
[**Accessibility**](https://getbootstrap.com/docs/5.3/getting-started/accessibility/): Key information for Accessibility concerns for the Bootstrap Framework
[**Forms**](https://getbootstrap.com/docs/5.3/forms/overview/): Provides controls for layouts, components for forms, etc. This is a page that provides examples and usage guidelines.

## External Links

[Welcome to django-bootstrap-v5’s documentation!](https://django-bootstrap-v5.readthedocs.io/en/latest/index.html)
[W3 Schools DJango and Bootstrap](https://www.w3schools.com/django/django_add_bootstrap5.php)
[Youtube: Tech with Tim](https://www.youtube.com/watch?v=0mCZdemSsbs)
[Youtbe: Keep Coding](https://www.youtube.com/watch?v=zglBdzzoDjM)



