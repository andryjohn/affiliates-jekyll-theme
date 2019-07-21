---
layout:     post
title:      JavaScript Questions
date:       2019-05-28
author: Andry
featured: true
categories: [ JavaScript, interviews, test ]
image: images/js.jpg

---

Test how well you know JavaScript, refresh your knowledge a bit, or prepare for your coding interview!
The answers are in the collapsed sections below the questions, simply click on them to expand it. Good luck!



---

## 1. What's the output?

```javascript
function sayHi() {
  console.log(name);
  console.log(age);
  var name = "Lydia";
  let age = 21;
}

sayHi();

```

- A: `Lydia` and `undefined`
- B: `Lydia` and `ReferenceError`
- C: `ReferenceError` and `21`
- D: `undefined` and `ReferenceError`

<details><summary><b>Answer</b></summary>


<strong>Answer: D</strong>

<p>Within the function, we first declare the <mark>name</mark> variable with the <mark>var</mark> keyword.</p>

<p>This means that the variable gets hoisted (memory space is set up during the creation phase) with the default value of <mark>undefined</mark> until we actually get to the line where we define the variable. We haven't defined the variable yet on the line where we try to log the  <mark>name</mark> variable, so it still holds the value of  <mark>undefined</mark>.</p>

<p>Variables with the <mark>let</mark> keyword (and <mark>const</mark>) are hoisted, but unlike <mark>var</mark>, don't get <i>initialized</i>. They are not accessible before the line we declare (initialize) them. This is called the "temporal dead zone". When we try to access the variables before they are declared, JavaScript throws a <mark>ReferenceError</mark>.
</p>
</details>

---

## 2. What's the output?

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i+
  setTimeout(() => console.log(i), 1);
}
```

- A: `0 1 2` and `0 1 2`
- B: `0 1 2` and `3 3 3`
- C: `3 3 3` and `0 1 2`

<details><summary><b>Answer</b></summary>

<strong>Answer: C</strong>

<p>Because of the event queue in JavaScript, the <mark>setTimeout</mark> callback function is called _after_ the loop has been executed. Since the variable <mark>i</mark> in the first loop was declared using the <mark>var</mark> keyword, this value was global. During the loop, we incremented the value of <mark>i</mark> by <mark>1</mark> each time, using the unary operator <mark>++</mark>. By the time the <mark>setTimeout</mark> callback function was invoked, <mark>i</mark> was equal to <mark></mark>` in the first example.</p>

<p>In the second loop, the variable <mark>i</mark> was declared using the <mark>let</mark> keyword: variables declared with the <mark>let</mark> (and <mark>const</mark>) keyword are block-scoped (a block is anything between <mark>{ }</mark>). During each iteration, <mark>i</mark> will have a new value, and each value is scoped inside the loop.</p>
</details>

---

## 3. What's the output?

```javascript
const shape = {
  radius: 10,
  diameter() {
    return this.radius * 2;
  },
  perimeter: () => 2 * Math.PI * this.radius
};

shape.diameter();
shape.perimeter();
```

- A: `20` and `62.83185307179586`
- B: `20` and `NaN`
- C: `20` and `63`
- D: `NaN` and `63`

<details><summary><b>Answer</b></summary>


<strong>Answer: B</strong>

<p>Note that the value of <mark>diameter</mark> is a regular function, whereas the value of <mark>perimeter</mark> is an arrow function.<br>

With arrow functions, the <mark>this</mark> keyword refers to its current surrounding scope, unlike regular functions! This means that when we call <mark>perimeter</mark>, it doesn't refer to the shape object, but to its surrounding scope (window for example).<br>

There is no value <mark>radius</mark> on that object, which returns <mark>undefined</mark>.

</p>
</details>

---

## 4. What's the output?

```javascript
+true;
!"Lydia";
```

- A: `1` and `false`
- B: `false` and `NaN`
- C: `false` and `false`

<details><summary><b>Answer</b></summary>

<strong>Answer: A</strong>

<p>
The unary plus tries to convert an operand to a number. <mark>true</mark> is <mark>1</mark>, and <mark>false</mark> is <mark>0</mark>.<br>

The string <mark>'Lydia'</mark> is a truthy value. What we're actually asking, is "is this truthy value falsy?". This returns <mark>false</mark>.

</p>
</details>

---

## 5. Which one is true?

```javascript
const bird = {
  size: "small"
};

const mouse = {
  name: "Mickey",
  small: true
};
```

- A: `mouse.bird.size` is not valid
- B: `mouse[bird.size]` is not valid
- C: `mouse[bird["size"]]` is not valid
- D: All of them are valid

<details><summary><b>Answer</b></summary>


<strong>Answer: A</strong>

<p>In JavaScript, all object keys are strings (unless it's a Symbol). Even though we might not _type_ them as strings, they are always converted into strings under the hood.<br>

JavaScript interprets (or unboxes) statements. When we use bracket notation, it sees the first opening bracket `[` and keeps going until it finds the closing bracket `]`. Only then, it will evaluate the statement.<br>

`mouse[bird.size]`: First it evaluates `bird.size`, which is <mark>"small"</mark>. <mark>mouse["small"]</mark> returns <mark>true</mark> <br>

However, with dot notation, this doesn't happen. <mark>`mouse`</mark> does not have a key called <mark>`bird`,</mark> which means that <mark>mouse.bird</mark> is <mark>`undefined`</mark>. Then, we ask for the `size` using dot notation: <mark>`mouse.bird.size`.</mark> Since <mark>mouse.bird</mark> is <mark>undefined</mark>, we're actually asking <mark>`undefined.size`</mark>. This isn't valid, and will throw an error similar to <mark> Cannot read </mark>property "size" of undefined.

</p>
</details>
<style>
mark {
background-color: #252525;
color: yellow;
padding-left: 5px;
padding-right: 5px;
padding-bottom: 5px;
box-shadow: 0 0 5px rgba(0,0,0,0.3);
border-radius: 5px;
}

:focus {
    outline: none!important;
}

</style>
