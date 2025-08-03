# 🎓 CSS `display` Property – Beginner Tutorial

## 🧾 Introduction

In CSS, the `display` property determines how an HTML element is rendered in the layout.

---

## 🧱 Common Display Values

| Display Type   | Description                                             |
| -------------- | ------------------------------------------------------- |
| `block`        | Takes up full width and starts on a new line            |
| `inline`       | Stays within line flow, no control over width/height    |
| `inline-block` | Flows inline, but allows width, height, padding, margin |

---

## 📄 HTML & CSS Demo

### ✅ Step 1: Code Setup

Paste this code into your HTML file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CSS Display Demo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }

    h2 {
      margin-top: 40px;
    }

    .demo-box {
      padding: 10px;
      margin: 5px;
      border: 2px solid #333;
      background-color: #f0f0f0;
    }

    .block {
      display: block;
      width: 100%;
      background-color: #a8dadc;
    }

    .inline {
      display: inline;
      background-color: #f4a261;
    }

    .inline-block {
      display: inline-block;
      width: 150px;
      background-color: #90be6d;
    }
  </style>
</head>
<body>

  <h1>CSS <code>display</code> Property Demo</h1>

  <h2>1. Block</h2>
  <div class="demo-box block">Block Element 1</div>
  <div class="demo-box block">Block Element 2</div>
  <p>✅ Takes full width and starts on a new line.</p>

  <h2>2. Inline</h2>
  <span class="demo-box inline">Inline 1</span>
  <span class="demo-box inline">Inline 2</span>
  <p>✅ Flows with text. Width and height cannot be set.</p>

  <h2>3. Inline-block</h2>
  <div class="demo-box inline-block">Inline-block 1</div>
  <div class="demo-box inline-block">Inline-block 2</div>
  <p>✅ Flows inline but allows width, height, margin, and padding.</p>

</body>
</html>
```

---

## 🔎 Explanation of Each Display Type

### 🟦 `block`

* Examples: `<div>`, `<h1>`, `<p>`, `<section>`
* Takes full width of the parent container
* Starts on a new line
* You can set width, height, padding, and margin

---

### 🟨 `inline`

* Examples: `<span>`, `<a>`, `<strong>`
* Stays inline with other elements
* Cannot have custom width or height
* Good for styling small parts of text

---

### 🟩 `inline-block`

* Behaves like `inline`, but:

  * You **can** set width and height
  * Ideal for buttons, nav links, cards

---

## 🧪 Exercise for Students

Ask students to:

* Change the `width` of the `inline` box — observe that it doesn’t work
* Add `padding` or `margin` to `inline-block` and see how it affects layout
* Try setting `display: none` to hide one of the boxes

---

## 📌 Bonus Tip

Teach students how `display` works with layout models like:

* `display: flex`
* `display: grid`

But **start with block and inline concepts** to build a strong foundation.
