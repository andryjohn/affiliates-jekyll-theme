---
layout:     post
title:      2-hours Landing Page
date:       2019-11-17
summary: 2 hour landing, learn HTML and CSS
categories: [ JavaScript, beginner, introduction ]
mathjax: true
courses: true
image: images/havas.gif
---

>2 hour landing, learn HTML and CSS

<iframe src="//www.slideshare.net/slideshow/embed_code/key/yvJzqzoUqqn7Td" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>


### 1. LET'S SET UP

1. Start Sublime Text. It will open a new black window.

2. Create a folder landing on your Desktop. Drag & drop this folder in the Sublime Text window.

3. In Sublime Text left navigation: Right click "New file"

4. Save it as index.html with `Cmd + S` or `Ctrl + S`

5. Do the same to create a `style.css` file


#### 2. ADD SOME HTML CONTENT


1. start with this HTML code in index.html


```html
<html>
  <head>
    <meta charset="utf-8">
    <title>My Awesome app</title>
  </head>
  <body>
    <h1>My Awesome app</h1>
    <p>This is the important line everyone reads..</p>
    <p>
      <a href="#">Start now</a>
    </p>

<i class="fa fa-3x fa-battery-full"></i>
   <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished

          </p>
<i class="fa fa-3x fa-battery-full"></i>
  <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
 <i class="fa fa-3x fa-check-circle"></i>
   <h2>Satisfaction</h2>
     <p>Your satisfaction is our priority</p>

<p>This is an awesome landing ©Codedot</p>
  </body>
</html>
```


**Then to save time, we just use a fontawesome icons for our features, so, in your `head`**



```html
<head>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
</head>
```

  <div class="icon list-inline" style="padding: 10px; margin: 10px;">
  <i class="fa fa-3x fa-truck"></i>
  <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished
          </p>
<i class="fa fa-3x fa-battery-full"></i>
  <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
 <i class="fa fa-3x fa-check-circle"></i>
<h2>Satisfaction</h2>
<p>Your satisfaction is our priority everyday!</p>

</div>

**Tips:** Also stay tuned checking icon resources on Product Hunt

<a href="https://www.producthunt.com/posts/animated-icons-pack?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-animated-icons-pack" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=148270&theme=light" alt="Animated Icons Pack - A pack of 100 animated vector icons. | Product Hunt Embed" style="width: 250px; height: 54px;" width="250px" height="54px" /></a>


#### 3. CSS FOR FONTS & COLORS

Link your stylesheet `style.css` in the `head` section of your HTML

```html
<head>
  <link href='style.css' rel='stylesheet'>
</head>
```
Then `copy/paste` the CSS code below in `style.css` and fix it cause it's ugly

1. For fonts use Google Fonts
2. For colors use Colorzilla Chrome plugin to pick
3. colors from other websites
4. You can also find nice colors on Coolors or Color Hunt

```css
/* style.css */
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
#### 4. WRAP WITH `DIV`

```html
<html>
  <head>
    <meta charset="utf-8">
    <title>My Awesome app</title>
  </head>
  <body>
  <div>
    <h1>My Awesome app</h1>
    <p>This is the important line everyone reads..</p>
    <p>
      <a href="#">Start now</a>
    </p>
  </div>

  <div>
 <h1>My Awesome app</h1>
    <p>This is the important line everyone reads..</p>
    <p>
      <a href="#">Start now</a>
    </p>
</div>
<div>
<i class="fa fa-3x fa-battery-full"></i>
   <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished

          </p>
</div>
<div>
  <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
</div>
<div>
 <i class="fa fa-3x fa-check-circle"></i>
 <h2>Satisfaction</h2>
 <p>Your satisfaction is our priority</p>
</div>

<div>
    <p>This is an awesome landing ©Codedot</p>
</div>
  </body>
</html>


```
#### 5. Footer:

and then the footer

```html
<ul>
  <li><a href="#"><i class="fab fa-youtube"></i></a></li>
  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
  <li><a href="#"><i class="fab fa-twitter"></i></a></li>
  <li><a href="#"><i class="fab fa-github"></i></a></li>
</ul
```
