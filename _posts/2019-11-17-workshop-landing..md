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

Time to discover HTML and CSS by coding our very first landing page!

To proceed, make sure you have the following programs installed on your laptop:


* [Sublime Text](), the text editor ;

* [Google Chrome]() - the best browser for developers.

#### Main takeaways

##### HTML basics

`HTML` is a language that defines the structure and content of your web page. Every `HTML` page has the same skeleton:

```html
<html>
  <head>
    <!-- page's intelligence (metadata) -->
    <meta charset="utf-8">
    <title>My playground landing</title>
    <link rel="stylesheet" href="style.css">
  </head>

  <body>
    <!-- page's content -->
    <h1>Awesome Product</h1>
    <p>This is the important line everyone reads..</p>
    <a href="#">Start Learning Now</a>
  </body>
</html>
```
#### HTML main syntax

`HTML` has a ton of different tags. Each tag has its own purpose, for example:

`<h1>`, `<h2>`,  `<h3>`, `<h4>` and `<h5>` are used for headers and subheaders (titles)
`<p>` for paragraphs of text
`<a>`for links
`<ul>`for unordered (i.e. not-numbered) lists and `<li>` for the list items inside that list
`<div>`used to wrap content into divisions of your web page, allowing you to manipulate groups of elements
There are loads more tags - you’ll learn them soon!

The syntax of an HTML element is always the same:

all content is wrapped between an opening `<tag>` and a closing `</tag>`;
the opening tag is mostly plain, but it can also specify attributes with values, such as the href attribute for a link, where the hyperlink is written inside the tag:

```html
<a href="http://www.codedot.fr">Codedot</a>
```
Some elements - such as `<img>` - don’t have closing tags. They just have attributes inside:

```html
<!-- images don't have closing tags -->
<img src="logo.png" alt="Codedot logo">
```
We call these self-closing tags.

##### HTML indentation

Indenting your code is ⚠️ very important ⚠️ when you start coding:

Your code needs to be readable by the future you 😣 or by your teammates 😖😫😩.
Not only is it easier to read and maintain, but if you ever get syntax errors you’ll be able to debug it in the blink of an eye!

It’s crucial to form good habits from the very beginning. Indenting will soon become as natural as breathing 🌬.

To properly indent your HTML code, each opening `<tag>` and associated closing `</tag>` must be vertically aligned. Any nested content should then be indented 1 tab right (= 2 spaces). Here is an example of good indentation:

```html
<div class="banner">
  <div class="banner-content">
    <h1>Hello World!</h1>
    <p>
      At the end of Le Wagon bootcamp I'll know:
      <ul>
        <li>Ruby</li>
        <li>SQL</li>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
        <li>Rails</li>
      </ul>
    </p>
  </div>
</div>
```
Properly indented HTML code should draw waves in your file 🌊🌊🌊 (or should look like a flying V of ducks if you prefer this metaphor 🦆🦆🦆).

#### Design in CSS

CSS is the language that gives style 🎨 to your HTML elements.

>Without CSS, web pages all have the same, boring and ugly look.

CSS selectors enable you to grab one or more elements, on which you can define style rules:

```css
p {
  color: red;
}
```
This will turn the text colour of all your <p> elements red!

##### Classes and IDs

Classes allow us to give multiple HTML elements the same name in order to change the css of all of them at the same time. IDs are only used when you want to manipulate one single element. For example:

```html
<a href="..." class="link-blue">Google</a>
<a href="..." id="link-codedot" >Le Wagon</a>
<a href="..." class="link-blue">Facebook</a>
```
To design our classes and IDs, we need to use selectors. class selectors start with a . and id selectors start with a #.

To design the blue links we must use a class selector:

```css
.link-blue {
  color: blue;
}
```
To design Le Codedt’s link, this time we use an id selector:

```css
#link-codedot {
  color: white;
  background-color: red;
}
```

##### Specificity of CSS selectors

CSS selectors have priority levels that define which style rule should be applied on an element. IDs are more specific than classes, which are more specific than tags. Any clashing style command will follow this order of priority. For instance consider the following image:

```html
<img src="..." class="img-big">
```
And the following CSS:

```css
img {
  width: 20px;
}
.img-big {
  width: 100px;
}
```
👉 The image will have a width of 100 pixels.

Now if the HTML is:

```html
<img src="..." class="img-big" id="logo">Google</a>
```
And the CSS is :

```css
img {
  width: 20px;
}
.img-big {
  width: 100px;
}
#logo {
  witdh: 50px;
}
```
👉 The image will have a width of 50 pixels.

Descendant selectors
You can also be more specific by combining selectors. For instance, to select all the links inside the element with the class="banner" you can use a descendant selector:

```css
.banner a {
  color: white;
}
```
#### Exercise

Your turn! It’s time to code your own landing page based on what you’ve learnt.
Share screenshots of your work on the forum 😎 (upload them to Dropbox for instance)

#### Resources

* Icons: [Icon store](), [The Noun Project](), [NucleoApp]()
* Fonts: [Google Fonts](https://fonts.google.com/)
* Colors: [Colorzilla]() , [Coolors](), [Color Hunt]()
* Background images: [Pexels]()
* CSS libraries: [Bootstrap]()


Happy Hacking and join us on [Meetup](https://www.meetup.com/fr-FR/Apprendre-le-developpement-web/) 🚀🚀🚀
