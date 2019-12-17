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
<iframe src="//www.slideshare.net/slideshow/embed_code/key/2pRkQlCVreEvf0" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/AndryRajohnson/2h-landing-page" title="2h landing page " target="_blank">2h landing page </a> </strong> from <strong><a href="https://www.slideshare.net/AndryRajohnson" target="_blank">AndryRajohnson</a></strong> </div>


### 1. LET'S SET UP

1. Start Sublime Text. It will open a new black window.

2. Create a folder landing on your Desktop. Drag & drop this folder in the Sublime Text window.

3. In Sublime Text left navigation: Right click "New file"

4. Save it as index.html with `Cmd + S` or `Ctrl + S`

5. Do the same to create a `style.css` file


#### 2. ADD SOME HTML CONTENT


1. start with this HTML code in index.html


```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">

  <title>My landing page</title>
</head>

<body>

<h1>Awesome Product</h1>
  <p>This is the important line everyone reads...</p>
        <a href="#">Buy now</a>

<i class="fab fa-5x fa-cc-apple-pay"></i>
   <h2>Easy to use</h2>
          <p>
            Pay with your mobile
          </p>

<i class="fab fa-5x fa-cc-apple-pay"></i>
   <h2>Easy</h2>
          <p>
            Pay with your mobile
          </p>
<i class="fas fa-5x fa-battery-full"></i>
   <h2>Fast shipping</h2>
   <p>  We make sure you recieve your product as soon as we have finished
</p>

<i class="fas fa-5x fa-shipping-fast"></i>
   <h2>Quality Assurance</h2>
    <p>  For every purchase you make, we will ensure there are no damages</p>

<i class="fas fa-5x fa-check-circle"></i>
   <h2>Satisfaction</h2>
    <p>Your satisfaction is our priority</p>

<p>This is an awesome landing by ©Codedot</p>
</body>
</html>

```


**Then we just use a fontawesome icons for our features, so, in your `head`**



```html
<head>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
</head>
```

  <div class="icon list-inline" style="padding: 10px; margin: 10px;">
<i class="fa fa-5x fa-cc-apple-pay"></i>
   <h2>Easy to use</h2>
          <p>
            Pay with your mobile
          </p>
  <i class="fa fa-5x fa-truck"></i>
  <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished
          </p>
<i class="fa fa-5x fa-battery-full"></i>
  <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
 <i class="fa fa-5x fa-check-circle"></i>
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

1. For fonts use [Google Fonts](https://fonts.google.com/specimen/Open+Sans?selection.family=Open+Sans)
2. For colors use [Colorzilla Chrome plugin to pick](https://www.colorzilla.com/chrome/)
3. colors from other [websites](https://codedot.tk)
4. You can also find nice colors on Coolors or [Color Hunt](https://colorhunt.co/)

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
    <title>Awesome Landing</title>
       <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
    <link href='style.css' rel='stylesheet'>

  </head>
  <body>
  <div id="banner">
 <h1>AWESOME PRODUCT</h1>
    <p>This is the important line everyone reads..</p>
    <p>
      <a href="#" class="btn btn-primary btn-lg">BUY NOW</a>
    </p>
</div>

    <div class="features">
<i class="fab fa-5x fa-cc-apple-pay"></i>
   <h2>Easy to use</h2>
          <p>
            Pay with your mobile
          </p>
</div>
  </div>

    <div class="features">
<i class="fas fa-5x fa-battery-full"></i>
 <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
</div>
  </div>
    <div class="features">
<i class="fas fa-5x fa-shipping-fast"></i>
 <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished

          </p>

</div>
  </div>
    <div class="features">
 <i class="fas fa-5x fa-check-circle"></i>
 <h2>Satisfaction</h2>
 <p>Your satisfaction is our priority</p>
</div>
 </div>



<div id="footer">
    <p>This is an awesome landing ©Codedot</p>
<ul>
  <li><a href="#"><i class="fab fa-youtube"></i></a></li>
  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
  <li><a href="#"><i class="fab fa-twitter"></i></a></li>
  <li><a href="#"><i class="fab fa-github"></i></a></li>
</ul>
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
**Have fun apply your own design**

```css
/* style.css */
*{
  margin: 0;
padding: 0;
}
body{
  background: rgb(245,245,245);
  color: #202020;
  font-size: 15px;
  font-family:  'Open Sans', sans-serif;;
}
h1{
  color: #202020;
  font-weight: bold;
  font-size: 35px;
}
h2 {
  color: #252525;
  font-weight: lighter;
  font-size: 25px;
}
a {
  color: green;
}
a:hover {
  text-decoration: none;
  color: green-light;
}
#banner{
  text-align: center;
  background-image: linear-gradient(90deg, rgba(0,0,0,0.4) 3%, rgba(0,0,0,0.4) 50%), url("https://unsplash.it/1300/600?party");
  background-size: cover;
  padding: 250px;
  text-shadow: 1px 1px 3px black;
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

#### 6. Start with bootstrap:


```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Bootstrap 101 Template</title>

    <!-- Bootstrap -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://code.jquery.com/jquery-1.12.4.min.js" integrity="sha384-nvAa0+6Qg9clwYCGGPpDQLVpLNn0fRaROjHqs13t4Ggj3Ez50XnGQqc/r8MhnRDZ" crossorigin="anonymous"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </body>
</html>
```
#### Just copy/paste let's play and see the result

Mobile first
With Bootstrap 2, we added optional mobile friendly styles for key aspects of the framework.

With Bootstrap 3, we've rewritten the project to be mobile friendly from the start.

Instead of adding on optional mobile styles, they're baked right into the core. In fact, Bootstrap is mobile first. Mobile first styles can be found throughout the entire library instead of in separate files.



```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Landing 2 hours</title>

    <!-- Bootstrap -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
    <link href='style.css' rel='stylesheet'>

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
   <div id="banner">
 <h1>AWESOME PRODUCT</h1>
    <p>This is the important line everyone reads..</p>
    <p>
      <a href="#" class="btn btn-primary btn-lg">BUY NOW</a>
    </p>
</div>
<div class="features text-center">
<i class="fab fa-5x fa-cc-apple-pay"></i>
   <h2>Easy to use</h2>
          <p>
            Pay with your mobile
          </p>
</div>
<div class="features text-center">
<i class="fas fa-5x fa-battery-full"></i>
   <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished

          </p>
</div>
<div class="features text-center">
<i class="fas fa-5x fa-shipping-fast"></i>
  <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
</div>
<div class="features text-center">
 <i class="fas fa-5x fa-check-circle"></i>
 <h2>Satisfaction</h2>
 <p>Your satisfaction is our priority</p>
</div>

<div id="footer">
    <p>This is an awesome landing ©Codedot</p>
<ul class="list-inline">
  <li><a href="#"><i class="fab fa-youtube"></i></a></li>
  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
  <li><a href="#"><i class="fab fa-twitter"></i></a></li>
  <li><a href="#"><i class="fab fa-github"></i></a></li>
</ul>
</div>

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://code.jquery.com/jquery-1.12.4.min.js" integrity="sha384-nvAa0+6Qg9clwYCGGPpDQLVpLNn0fRaROjHqs13t4Ggj3Ez50XnGQqc/r8MhnRDZ" crossorigin="anonymous"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </body>
</html>

```
#### 7. Responsive

```html
<div class="container">
<div class="row">
  <div class="col-xs-12 col-sm-6-col-md-3"></div>
  <div class="col-xs-12 col-sm-6-col-md-3"></div>
  <div class="col-xs-12 col-sm-6-col-md-3"></div>
  <div class="col-xs-12 col-sm-6-col-md-3"></div>
</div>
</div>
```
#### 8. Final result:

```html


<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Landing 2 hours</title>

    <!-- Bootstrap -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css">
    <link href='style.css' rel='stylesheet'>

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
   <div id="banner">
 <h1>AWESOME PRODUCT</h1>
    <p>This is the important line everyone reads..</p>
    <p>
      <a href="#" class="btn btn-primary btn-lg">BUY NOW</a>
    </p>
</div>

<div class="container">
<div class="row">
  <div class="col-xs-12 col-sm-6 col-md-3">
    <div class="features text-center">
<i class="fab fa-5x fa-cc-apple-pay"></i>
   <h2>Easy to use</h2>
          <p>
            Pay with your mobile
          </p>
</div>
  </div>
  <div class="col-xs-12 col-sm-6 col-md-3">
    <div class="features text-center">
<i class="fas fa-5x fa-battery-full"></i>
 <h2>Quality Assurance</h2>
          <p>
            For every purchase you make, we will ensure there are no damages
          </p>
</div>
  </div>
  <div class="col-xs-12 col-sm-6 col-md-3">
    <div class="features text-center">
<i class="fas fa-5x fa-shipping-fast"></i>
 <h2>Fast Shipping</h2>
          <p>
            We make sure you recieve your product as soon as we have finished

          </p>

</div>
  </div>
  <div class="col-xs-12 col-sm-6 col-md-3">
    <div class="features text-center">
 <i class="fas fa-5x fa-check-circle"></i>
 <h2>Satisfaction</h2>
 <p>Your satisfaction is our priority</p>
</div>

  </div>
</div>
</div>


<div id="footer">
    <p>This is an awesome landing ©Codedot</p>
<ul class="list-inline">
  <li><a href="#"><i class="fab fa-youtube"></i></a></li>
  <li><a href="#"><i class="fab fa-facebook"></i></a></li>
  <li><a href="#"><i class="fab fa-twitter"></i></a></li>
  <li><a href="#"><i class="fab fa-github"></i></a></li>
</ul>
</div>

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://code.jquery.com/jquery-1.12.4.min.js" integrity="sha384-nvAa0+6Qg9clwYCGGPpDQLVpLNn0fRaROjHqs13t4Ggj3Ez50XnGQqc/r8MhnRDZ" crossorigin="anonymous"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </body>
</html>
```

```css
/* style.css */
*{
  margin: 0;
padding: 0;
}
body{
  background: rgb(245,245,245);
  color: #202020;
  font-size: 15px;
  font-family:  'Open Sans', sans-serif;;
}
h1{
  color: #202020;
  font-weight: bold;
  font-size: 35px;
}
h2 {
  color: #252525;
  font-weight: lighter;
  font-size: 25px;
}
a {
  color: green;
}
a:hover {
  text-decoration: none;
  color: green-light;
}
#banner{
  text-align: center;
  background-image: linear-gradient(90deg, rgba(0,0,0,0.4) 3%, rgba(0,0,0,0.4) 50%), url("https://unsplash.it/1300/600?party");
  background-size: cover;
  padding: 250px;
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
