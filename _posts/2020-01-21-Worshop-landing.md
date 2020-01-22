---
layout:     post
title:      2-hours Landing Page guides
date:       2020-01-21
summary: 2 hour landing, learn HTML and CSS
categories: [ HTML, CSS, beginner, introduction ]
mathjax: true
courses: true
image: images/landing.jpg
---

<iframe src="//www.slideshare.net/slideshow/embed_code/key/2pRkQlCVreEvf0" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/AndryRajohnson/2h-landing-page" title="2h landing page " target="_blank">2h landing page </a> </strong> from <strong><a href="https://www.slideshare.net/AndryRajohnson" target="_blank">AndryRajohnson</a></strong> </div>

## 1. LET'S SET UP

1. Start Sublime Text. It will open a new black window.
2. Create a **folder** `landing` on your Desktop. Drag & drop this folder in the Sublime Text window.

3. In Sublime Text left navigation:

* Right click `"New file"`
* Save it as index.html with `Cmd + S` or `Ctrl + S`
* Do the same to create a `style.css` file
* Then `"New Folder"` and create an images folder
* Finally **double click** on `index.html` to open it with Chrome

![setup](/images/setup.png)

## 2. ADD SOME HTML CONTENT

* Start with this HTML code in index.html

```html
<html>
  <head>
    <!-- page's intelligence (metadata) -->
    <meta charset="utf-8">
    <title>My playground landing</title>
  </head>

  <body>
    <!-- page's content -->
    <h1>Awesome Product</h1>
    <p>This is the important line everyone reads..</p>
    <a href="#">Start Learning Now</a>
  </body>
</html>
```

* To save time, In your `head`, it's in your `head` we'll use [Fontawesome](https://fontawesome.com/)!

```html
<head>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
</head>
```



And then

```html
<div class="features">
<i class="fa fa-3x fa-truck"></i>
   <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished

          </p>
</div>
<div class="features">
<i class="fa fa-3x fa-battery-full"></i>
  <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
</div>
<div class="features">
  <i class="fa fa-3x fa-check-circle"></i>
   <h2>Satisfaction</h2>
     <p>Your satisfaction is our priority</p>
</div>
<div id="footer">
<p>This is an awesome landing ©Codedot</p>
</div>

</body>
</html>

```

### 3. CSS FOR FONTS & COLORS

Link your stylesheet `style.css` in the `head` section of your `HTML`

```html
<head>
  <link href='style.css' rel='stylesheet'>
</head>
```
Then **copy/paste** the CSS code below in `style.css` and fix it cause it's ugly

* For fonts use [Google Fonts]()
* For colors use [Colorzilla Chrome]() plugin to pick colors from other websites
* You can also find nice colors on [Coolors]() or
[Color Hunt]()

```css
body{
  background: rgb(245,245,245);
  color: green;
  font-size: 25px;
  font-family: Helvetica;
}
h1{
  font-family: Courier;
  color: red;
  font-weight: lighter;
  font-size: 10px;
}
h2 {
  font-family: Courier;
  color: pink;
  font-weight: lighter;
  font-size: 8px;
}
a {
  color: yellow;
}
a:hover {
  text-decoration: none;
  color: purple;
}
```

## 4. WRAP WITH DIV

Wrap different sections in different `div` and name your `tag`

```html
<div class="features">
<i class="fa fa-3x fa-truck"></i>
   <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished

          </p>
</div>
<div class="features">
<i class="fa fa-3x fa-battery-full"></i>
  <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
</div>
<div class="features">
  <i class="fa fa-3x fa-check-circle"></i>
   <h2>Satisfaction</h2>
     <p>Your satisfaction is our priority</p>
</div>
<div id="footer">
<p>This is an awesome landing ©Codedot</p>
</div>

</body>
</html>

```
And add this nice `css` code

```css
html, body {
    margin: 0;
    padding: 0;
}

#banner{
  text-align: center;
  background-image: linear-gradient(90deg, rgba(0,0,0,0.4) 3%, rgba(0,0,0,0.4) 50%), url("https://unsplash.it/1300/600?random");
  background-size: cover;
  padding-top: 25vh;
  height: 75vh;
}
#banner h1 {
  color: #ffff;
  font-size: 60px;
}
#banner p {
  color: #ffff;
  opacity: 0.8;
  font-size: 35px;
  font-weight: lighter;
}
#footer{
  padding: 30px;
  background: rgb(30, 30, 30);
  color: lightgrey;
}
#footer{
  padding: 30px;
  background: rgb(30, 30, 30);
  color: lightgrey;
}
#footer a{
  font-size: 20px;
  color: lightgrey;
}
.features{
  padding: 50px;
  font-weight: lighter;
}


```
## 6. FOOTER

```html
<ul>
  <li><a href="#"><i class="fab fa-youtube"></i></a></li>
  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
  <li><a href="#"><i class="fab fa-twitter"></i></a></li>
  <li><a href="#"><i class="fab fa-github"></i></a></li>
</ul>
```
