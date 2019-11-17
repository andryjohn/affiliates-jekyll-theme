---
layout:     post
title:      Workshop Landing Page
date:       2019-11-17
summary: 2 hour landing, learn HTML and CSS
categories: [ JavaScript, beginner, introduction ]
mathjax: true
courses: true
image: images/branding.jpg
---

>2 hour landing, learn HTML and CSS

<iframe src="//www.slideshare.net/slideshow/embed_code/key/yvJzqzoUqqn7Td" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>


### 1. LET'S SET UP

1. Start Sublime Text. It will open a new black window.

2. Create a folder landing on your Desktop. Drag & drop this folder in the Sublime Text window.

3. In Sublime Text left navigation: Right click "New file"

4. Save it as index.html with `Cmd + S` or `Ctrl + S`

5. Do the same to create a `style.css` file

7. Then "New Folder" and create an images folder

8. Finally double click on index.html to open it with Chrome

![sublime](/images/setup.png)


#### 2. ADD SOME HTML CONTENT

1. to save time, just right-click on the following images and save them in your images folder



2. Then start with this HTML code in index.html


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

    <img src="images/briefcase.png" alt="picture description" width="100">
    <h2>Fast</h2>
    <p>A fast app, <strong>very fast</strong> app</p>

    <img src="images/diamond.png" alt="picture description" width="100">
    <h2>Simple</h2>
    <p>A simple app, <strong>very simple</strong> app</p>

    <img src="images/heart.png" alt="picture description" width="100">
    <h2>Awesome</h2>
    <p>An awesome app, <strong>very awesome</strong> app</p>

    <img src="images/laptop.png" alt="picture description" width="100">
    <h2>Beautiful</h2>
    <p>A beautiful app, <strong>very beautiful</strong> app</p>

    <p>This is an awesome landing ©Codedot</p>
  </body>
</html>
```
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
