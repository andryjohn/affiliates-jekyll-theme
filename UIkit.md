---
layout: default
title: Composants web avec HTML et CSS
mathjax: true
categorie: [ Components, design, Bootstrap, HTMl, CSS ]
---
# Components From Scratch
---
![airBnB](images/js.gif)

---


Components are a great way to design and develop your UI using smaller, reusable pieces with better consistency.


>In today’s ecosystem, UI components can also function as UX components, combining the power to create both functional and visual consistency.


You can design some compenents, then reuse them to build your *own product very quickly*. So let's *design*!


>*Most of the components have a dependency on [Bootstrap (4.3)](https://getbootstrap.com/) & [Fontawesome (5.7)](https://fontawesome.com/), so make sure you have the libraries in your project.*


#### Avatar:

So let's begin with a simple one, useful for your *profile* for example.

<img class="avatar" alt="avatar" src="https://kitt.lewagon.com/placeholder/users/cveneziani" />
<img class="avatar-large" alt="avatar-large" src="https://kitt.lewagon.com/placeholder/users/arthur-littm" />
<img class="avatar-bordered" alt="avatar-bordered" src="https://kitt.lewagon.com/placeholder/users/sarahlafer" />
<img class="avatar-square" alt="avatar-square" src="https://kitt.lewagon.com/placeholder/users/krokrob" />

<style>
  .avatar {
  width: 40px;
  border-radius: 50%;
}

.avatar-large {
  width: 56px;
  border-radius: 50%;
}

.avatar-bordered {
  width: 40px;
  border-radius: 50%;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}

.avatar-square {
  width: 40px;
  border-radius: 0px;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}

</style>
##### HTML


```html
<img class="avatar" alt="avatar" src="https://kitt.lewagon.com/placeholder/users/cveneziani" />
<img class="avatar-large" alt="avatar-large" src="https://kitt.lewagon.com/placeholder/users/arthur-littm" />
<img class="avatar-bordered" alt="avatar-bordered" src="https://kitt.lewagon.com/placeholder/users/sarahlafer" />
<img class="avatar-square" alt="avatar-square" src="https://kitt.lewagon.com/placeholder/users/krokrob" />

```
##### CSS
```css
.avatar {
  width: 40px;
  border-radius: 50%;
}

.avatar-large {
  width: 56px;
  border-radius: 50%;
}

.avatar-bordered {
  width: 40px;
  border-radius: 50%;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}

.avatar-square {
  width: 40px;
  border-radius: 0px;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}
```

#### Button design:

Then, **Button**, I choose to design two kind of button, [*Medium*](https://medium.com/) and [*Treehouse*](https://teamtreehouse.com/).

<html>
<div class="container">
       <a href="#" class="btn-medium">Write stories</a>
         <a href="#" class="btn-treehouse">Free trial</a>
         <a class="btn btn-gradient" href="#">Start now</a>
     </div>
<style>
  .container {
    padding: 2rem;
  }

  .btn-medium {

  color: #999999;
  border: 1px solid #999999;
  padding: 10px 15px;
  border-radius: 50px;
  font-weight: lighter;
  opacity: 0.6;
}

.btn-medium:hover {
  opacity: 1;
  text-decoration: none;
  color: #999999;
}

.btn-treehouse {
  color: white;
  padding: 10px 15px;
  border-radius: 4px;
  font-weight: bold;
  background: #6AD58B;
  opacity: 0.8;
}

.btn-treehouse:hover {
  opacity: 1;
  background: #6AD58B;
  text-decoration: none;
  color: white;
}
.btn-gradient {
  color: white;
  padding: 10px 15px;
  border-radius: 4px;
  font-weight: bold;
  background: linear-gradient(#167FFB, #0F60C4);
  transition: background 0.3s ease;
  border: 1px solid #0F60C4;
}

.btn-gradient:hover {
  background: linear-gradient(#147EFF, #0F67DA);
  color: white;
}
</style>
</html>


##### HTML
```html
  <div class="container">
    <h2>Button design</h2>
       <a href="#" class="btn-medium">Write stories</a>
         <a href="#" class="btn-treehouse">Start now</a>
     </div>

```
##### CSS

```css
.btn-medium {
  color: #999999;
  border: 1px solid #999999;
  padding: 10px 15px;
  border-radius: 50px;
  font-weight: lighter;
  opacity: 0.6;
}

.btn-medium:hover {
  opacity: 1;
  text-decoration: none;
  color: #999999;
}

.btn-treehouse {
  color: white;
  padding: 10px 15px;
  border-radius: 4px;
  font-weight: bold;
  background: #6AD58B;
}

.btn-treehouse:hover {
  opacity: 1;
  background: #6AD58B;
  text-decoration: none;
  color: white;
}
```

---

#### Alerts!
<!--rendering Alert-->
<div class="container">
<div class="flash flash-success alert alert-dismissible fade show" role="alert">
  <span><strong>Yay!</strong> 🎉 you successfully signed in to our service.</span>
</div>

<div class="flash flash-warning alert alert-dismissible fade show" role="alert">
  <span><strong>Mmh</strong> 🤔 seems like you don't have <a href="#">profile picture</a> yet.</span>
</div>

<div class="flash flash-danger alert alert-dismissible fade show" role="alert">
  <span><strong>Oops!</strong> 😱 a problem has occurred while processing your booking.</span>
</div>
</div>
<style>
.flash {
  padding: 16px 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: whitesmoke;
  box-shadow: 0 0 8px rgba(0,0,0,0.2);
  border-radius: 4px;
  margin: 8px;
}

.flash-success {
  border: 2px solid #1EDD88;
}

.flash-warning {
  border: 2px solid #FFC65A;
}

.flash-danger {
  border: 2px solid #FD1015;
}
.flash:hover {
  webkit-transform: scale(1.005);
  -moz-transform: scale(1.005);
  -ms-transform: scale(1.005);
  -o-transform: scale(1.005);
  transform: scale(1.005);
  transition: 0.9s;

}
</style>


##### HTML

```html
<div class="flash flash-success alert alert-dismissible fade show" role="alert">
  <span><strong>Yay!</strong> 🎉 you successfully signed in to our service.</span>
</div>

<div class="flash flash-warning alert alert-dismissible fade show" role="alert">
  <span><strong>Mmh</strong> 🤔 seems like you don't have <a href="#">profile picture</a> yet.</span>
</div>

<div class="flash flash-danger alert alert-dismissible fade show" role="alert">
  <span><strong>Oops!</strong> 😱 a problem has occurred while processing your booking.</span>
</div>

```
##### CSS
```css
.flash {
  padding: 16px 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: whitesmoke;
  box-shadow: 0 0 8px rgba(0,0,0,0.2);
  border-radius: 4px;
  margin: 8px;
}

.flash-success {
  border: 2px solid #1EDD88;
}

.flash-warning {
  border: 2px solid #FFC65A;
}

.flash-danger {
  border: 2px solid #FD1015;
}
.flash:hover {
  webkit-transform: scale(1.2);
  -moz-transform: scale(1.2);
  -ms-transform: scale(1.2);
  -o-transform: scale(1.2);
  transform: scale(1.2);
  transition: 0.9s;

}

```
---

#### Cards design:

Let's move on! The next one is, **cards**
<div class="container">
 <div class="row">
    <div class="col-xs-12 col-sm-4">
    <div class="card" style="background-image: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.2)), url('https://source.unsplash.com/6ZWhi3YhDY8');">
  <div class="card-category">Popular</div>
  <div class="card-description">
    <h2>Breakfast</h2>
    <p>Awesome</p>
  </div>
  <img class="card-user" src="https://source.unsplash.com/OjvZ_2vSruk">
  <a class="card-link" href="#" ></a>
</div>
    </div>
    <div class="col-xs-12 col-sm-4">
  <div class="card" style="background-image: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.2)), url('https://source.unsplash.com/osblobZQL8c');">
  <div class="card-category">Popular</div>
  <div class="card-description">
    <h2>Brunch</h2>
    <p>Lovely place, "the best place"</p>
  </div>
  <img class="card-user" src="https://source.unsplash.com/OjvZ_2vSruk">
  <a class="card-link" href="#" ></a>
</div>
    </div>
    <div class="col-xs-12 col-sm-4">
      <!-- insert <div class="card"> --><div class="card" style="background-image: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.2)), url('https://source.unsplash.com//JnFGgVaFpmE');">
  <div class="card-category">Popular</div>
  <div class="card-description">
    <h2>Asian Foods</h2>
    <p>Awesome place,we Love it!</p>
  </div>
  <img class="card-user" src="https://source.unsplash.com/OjvZ_2vSruk">
  <a class="card-link" href="#" ></a>
</div>
    </div>
  </div>
  </div>

<style>

.card {
  width: 18em;
  height: 10em;
  text-shadow: 0 1px 3px rgba(0,0,0,0.6);
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
  background-size: cover !important;
  background-position: center;
  color: whitesmoke;
  position: relative;
  border-radius: 7px;
  margin: 10px;
}
.card-user {
  position: absolute;
  right: 10px;
  top: 10px;
  width: 60px;
  border-radius: 50%;
  height: 55px;
}
.card-category {
  position: absolute;
  font-family: 'Roboto', sans-serif;
  top: 10px;
  left: 10px;
  font-size: 25px;
  text-transform: uppercase;
}
.card-description {
  position: absolute;
  bottom: 10px;
  left: 10px;
}
.card-description h2 {

  font-size: 15px;
  font-weight: bold;
}
.card-description p {
  font-size: 12px;
  opacity: 0.7;
  font-weight: lighter;
  color: #ffff;
}
.card-link {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  z-index: 2;
  background: black;
  opacity: 0;
}
.card:hover {
   margin: 10px;
   webkit-transform: scale(1.1);
  -moz-transform: scale(1.1);
  -ms-transform: scale(1.1);
  -o-transform: scale(1.1);
  transform: scale(1.1);
  transition: 0.9s;
}
</style>



##### HTML

```html
  <h2>Card design</h2>
      <div class="row">
        <div class="col-xs-12 col-sm-4">
          <div class="card">
            <img src="./ladies.jpeg" alt="" class="avatar card-user">
            <span class="card-category">POPULAR</span>
            <div class="card-description">
              <h3>Stripe</h3>
              <p>A cool payment API</p>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-sm-4">
          <div class="card">
            <img src="./ladies.jpeg" alt="" class="avatar card-user">
            <span class="card-category">POPULAR</span>
            <div class="card-description">
              <h3>Stripe</h3>
              <p>A cool payment API</p>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-sm-4">
          <div class="card">
            <img src="./ladies.jpeg" alt="" class="avatar card-user">
            <span class="card-category">POPULAR</span>
            <div class="card-description">
              <h3>Stripe</h3>
              <p>A cool payment API</p>
            </div>
          </div>
        </div>
      </div>
```

##### CSS

```css
.card {
  position: relative;
  height: 175px;
  background: linear-gradient(-225deg, rgba(30,30,30,0.6) 30%, rgba(46,46,46,0.5) 80%), url("http://unsplash.it/400/300/?random");
  background-size: cover;
  color: white;
}

.card-user {
  border-radius: 50%;
  position: absolute;
  top: 10px;
  right: 10px;
}
.card-category {
  position: absolute;
  top: 10px;
  left: 10px;
}
.card-description {
  position: absolute;
  bottom: 10px;
  left: 10px;
}
```

---

#### Card product :


<div class="card-product">
  <img src="https://images.unsplash.com/photo-1517336714731-489689fd1ca8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=926&q=80">
  <div class="card-product-infos">
    <h2>Macbook Pro</h2>
    <p>Product description with <strong>relevant info</strong> only.</p>
   </div>
</div>
<style>


.card-product {
  margin: 35px;
  overflow: hidden;
  height: 120px;
  background: white;
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
  display: flex;
  align-items: center;
  cursor: pointer;
}

.card-product img {
  height: 100%;
  width: 120px;
  object-fit: cover;
  border-radius: none!important;
}

.card-product h2 {
  font-size: 16px;
  font-weight: bold;
  margin: 0;
}

.card-product p {
  font-size: 12px;
  line-height: 1.4;
  opacity: .7;
  margin-bottom: 0;
  margin-top: 8px;
}

.card-product .card-product-infos {
  padding: 16px;
}

.card-product:hover {
  webkit-transform: scale(1.1);
  -moz-transform: scale(1.1);
  -ms-transform: scale(1.1);
  -o-transform: scale(1.1);
  transform: scale(1.1);
  transition: 0.8s;
}
</style>

##### HTML

```html
<div class="card-product">
  <img src="https://images.unsplash.com/photo-1517336714731-489689fd1ca8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=926&q=80">
  <div class="card-product-infos">
    <h2>Macbook Pro</h2>
    <p>Product description with <strong>relevant info</strong> only.</p>
   </div>
</div>
```
##### css

```css
.card-product {
  margin: 35px;
  overflow: hidden;
  height: 120px;
  background: white;
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
  display: flex;
  align-items: center;
  cursor: pointer;
}

.card-product img {
  height: 100%;
  width: 120px;
  object-fit: cover;
}

.card-product h2 {
  font-size: 16px;
  font-weight: bold;
  margin: 0;
}

.card-product p {
  font-size: 12px;
  line-height: 1.4;
  opacity: .7;
  margin-bottom: 0;
  margin-top: 8px;
}

.card-product .card-product-infos {
  padding: 16px;
}

.card-product:hover {
  webkit-transform: scale(1.1);
  -moz-transform: scale(1.1);
  -ms-transform: scale(1.1);
  -o-transform: scale(1.1);
  transform: scale(1.1);
  transition: 0.8s;
}
```
---

#### Card trip:

<div class="card-trip">
  <img src="https://source.unsplash.com/vO0hUESehtc">
  <div class="card-trip-infos">
    <div>
      <h2>Italia </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/DpPutJwgyW8">
  <div class="card-trip-infos">
    <div>
      <h2>Kyoto </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/oqFHLfLFtmc">
  <div class="card-trip-infos">
    <div>
      <h2>Japan </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>

  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/9sz0RKcPAQw">
  <div class="card-trip-infos">
    <div>
      <h2>Tokyo </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/QAwciFlS1g4">
  <div class="card-trip-infos">
    <div>
      <h2>Paris </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
  </div>
</div>

  <style>
.card-trip {
  margin: 35px;
  overflow: hidden;
  background: whitesmoke;
  box-shadow: 0 0 15px rgba(0,0,0,0.5);
}

.card-trip > img {
  height: 200px;
  width: 100%;
  object-fit: cover;
}

.card-trip h2 {
  font-size: 17px;
  font-weight: bold;
  margin: 0;
}

.card-trip p {
  font-size: 12px;
  opacity: 0.7;
  margin: 0;
}


.card-trip .card-trip-infos {
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  position: relative;
}

.card-trip-infos .card-trip-user {
  position: absolute;
  right: 16px;
  top: -20px;
  width: 45px;
  border-radius: 50%;
}
.card-trip:hover {
   webkit-transform: scale(1.05);
  -moz-transform: scale(1.05);
  -ms-transform: scale(1.05);
  -o-transform: scale(1.05);
  transform: scale(1.05);
  transition: 0.9s;
}
  </style>

##### HTML

```html
<div class="card-trip">
  <img src="https://source.unsplash.com/vO0hUESehtc">
  <div class="card-trip-infos">
    <div>
      <h2>Italia </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/MTZTGvDsHFY' class="card-trip-user avatar-bordered"/>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/DpPutJwgyW8">
  <div class="card-trip-infos">
    <div>
      <h2>Kyoto </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/ZHvM3XIOHoE' class="card-trip-user avatar-bordered"/>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/oqFHLfLFtmc">
  <div class="card-trip-infos">
    <div>
      <h2>Japan </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/ZHvM3XIOHoE' class="card-trip-user avatar-bordered"/>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/9sz0RKcPAQw">
  <div class="card-trip-infos">
    <div>
      <h2>Tokyo </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/ZHvM3XIOHoE' class="card-trip-user avatar-bordered"/>
  </div>
</div>
  <div class="card-trip">
  <img src="https://source.unsplash.com/QAwciFlS1g4">
  <div class="card-trip-infos">
    <div>
      <h2>Paris </h2>
      <p>Come to my hometown, wine and pasta an awesome place!</p>
    </div>
    <h2 class="card-trip-pricing">£199.99</h2>
    <img src='https://source.unsplash.com/MTZTGvDsHFY' class="card-trip-user avatar-bordered"/>
  </div>
</div>
```
##### CSS

```css
.card-trip {
  margin: 35px;
  overflow: hidden;
  background: whitesmoke;
  box-shadow: 0 0 15px rgba(0,0,0,0.5);
}

.card-trip > img {
  height: 200px;
  width: 100%;
  object-fit: cover;
}

.card-trip h2 {
  font-size: 17px;
  font-weight: bold;
  margin: 0;
}

.card-trip p {
  font-size: 12px;
  opacity: 0.7;
  margin: 0;
}


.card-trip .card-trip-infos {
  padding: 16px;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  position: relative;
}

.card-trip-infos .card-trip-user {
  position: absolute;
  right: 16px;
  top: -20px;
  width: 45px;
  border-radius: 50%;
}
.card-trip:hover {
   webkit-transform: scale(1.05);
  -moz-transform: scale(1.05);
  -ms-transform: scale(1.05);
  -o-transform: scale(1.05);
  transform: scale(1.05);
  transition: 0.9s;
}

```

#### Banner:

We've almost done, the last one is  **Banner**. Great for building your *landing page*!

<div class="container">
<div class="banner" style="background-image: linear-gradient(rgba(0,0,0,0.4),rgba(0,0,0,0.4)), url(/images/tech.jpg);">
  <div class="container">
    <h1>Learning code brings <strong>tech skills</strong> to <strong>creative people</strong>!</h1>
    <p>Change your life and learn to code at one of our campuses around the world.</p>
     <a href="#" class="btn-treehouse">Start now</a>
  </div>
</div>
</div>
<style>
.banner {
  margin-bottom:  3rem;
  background-size: cover;
  background-position: center;
  padding: 14rem 6rem;

}

.banner h1 {
  margin: 0;
  color: white;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
  font-size: 32px;
  font-weight: bold;
}

.banner p {
  font-size: 20px;
  color: white;
  opacity: .7;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
}
</style>


##### HTML
```html
<div class="banner" style="background-image: linear-gradient(rgba(0,0,0,0.4),rgba(0,0,0,0.4)), url(https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/background.png);">
  <div class="container">
    <h1>Learning code brings <strong>tech skills</strong> to <strong>creative people</strong>!</h1>
    <p>Change your life and learn to code at one of our campuses around the world.</p>
     <a href="#" class="btn-treehouse">Start now</a>
  </div>
</div>
```

##### CSS
```css
.banner {
  background-size: cover;
  background-position: center;
  padding: 150px 0;
}

.banner h1 {
  margin: 0;
  color: white;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
  font-size: 32px;
  font-weight: bold;
}

.banner p {
  font-size: 20px;
  color: white;
  opacity: .7;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
}
```


<!--personnal css-->
<style>
  .highlight {
  background-color: #F8F8F8;
  box-shadow: 0 0 5px rgba(0,0,0,0.1);
  border-radius: 3px;
}

</style>
<!--personnal css-->


#### Notification
<div class="container">
<div class="notification">
  <img src='https://kitt.lewagon.com/placeholder/users/arthur-littm' class="avatar-large" />
  <div class="notification-content">
    <p><small>14th January</small></p>
    <p>Lorem ipsum dolor sit amet, <strong>consectetur</strong> adipisicing elit.</p>
  </div>

  <div class="notification-actions">
    <a href="#">Edit <i class="fas fa-pencil-alt"></i></a>
    <a href="#">Delete <i class="far fa-trash-alt"></i></a>
  </div>
</div>

<div class="notification">
  <img src='https://kitt.lewagon.com/placeholder/users/Eschults' class="avatar-large"/>
  <div class="notification-content">
    <p><small>9th January</small></p>
    <p>Lorem ipsum dolor sit amet, <strong>consectetur</strong> adipisicing elit.</p>
  </div>

  <div class="notification-actions">
    <a href="#">Edit <i class="fas fa-pencil-alt"></i></a>
    <a href="#">Delete <i class="far fa-trash-alt"></i></a>
  </div>
</div>
</div>
<style>

  .notification {
  display: flex;
  align-items: center;
  margin-bottom: 8px;
  background: white;
  padding: 8px 16px;
  border: 1px solid rgb(235,235,235);
}

.notification .notification-content {
  flex-grow: 1;
  padding: 0 24px;
}

.notification p {
  margin: 0;
  line-height: 1.4;
}

.notification small {
  color: #999999;
  font-weight: bold;
}
.notification .notification-actions {
  opacity: 0;
  display: flex;
  transition: ease .3s;
}

.notification:hover .notification-actions {
  opacity: 1;
}

.notification .notification-actions a {
  color: #999999;
  margin-left: 16px;
  font-size: 14px;
}

.notification .notification-actions a:hover {
  color: #555555;
}
</style>


```html
<form novalidate="novalidate" class="simple_form search" action="/" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
  <div class="search-form-control form-group">
    <input class="form-control string required" type="text" name="search[query]" id="search_query" />
    <button name="button" type="submit" class="btn btn-flat">
      <i class="fas fa-search"></i> Search
    </button>
  </div>
</form>
```
#### css

```css
.search-form-control {
  position: relative;
}

.search-form-control .btn {
  position: absolute;
  top: 8px;
  bottom: 8px;
  right: 8px;
}

.search-form-control .form-control {
  height: 3.5rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
  border: 1px solid #E7E7E7;
}

.search-form-control .form-control:focus {
  border: 1px solid #1EDD88;
  outline: none !important;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
}
COPY
Tabs
Bookings
Requests
Conversations
HTML
CSS
 <ul class="list-inline tabs-underlined">
  <li>
    <a href="#" class="tab-underlined active">Bookings</a>
  </li>
  <li>
    <a href="#" class="tab-underlined">Requests</a>
  </li>
  <li>
    <a href="#" class="tab-underlined">Conversations</a>
  </li>
</ul>
```
  <footer><cite title="Workshop">Credit: Andry Rajohnson from "workshop le wagon UI"</cite></footer>

