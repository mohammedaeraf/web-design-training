# 🎓 **Flexbox Tutorial - Part 1: Flexbox Basics**

## 🧾 What is Flexbox?

Flexbox (Flexible Box Layout) is a modern layout system in CSS that makes it easier to **arrange elements in a row or column**, align them, and distribute space—even when their size is unknown.

---

## ✅ How to Enable Flexbox

To make an element a **flex container**, use:

```css
display: flex;
```

All direct children of this element become **flex items**.

---

## 📘 Part 1 Topics:

### 1. `display: flex`

### 2. `flex-direction`

### 3. `justify-content`

### 4. `align-items`

---

## 🧪 Example Code (Part 1)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Flexbox Part 1</title>
  <style>
    .container {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      height: 200px;
      border: 2px solid #ccc;
      margin: 20px;
    }

    .box {
      width: 100px;
      height: 100px;
      background-color: #3498db;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 5px;
    }
  </style>
</head>
<body>

  <h2>Flexbox Part 1: Basic Properties</h2>

  <div class="container">
    <div class="box">1</div>
    <div class="box">2</div>
    <div class="box">3</div>
  </div>

</body>
</html>
```

---

## 🔍 Explanation of Properties

### 1️⃣ `flex-direction`

| Value            | Description                     |
| ---------------- | ------------------------------- |
| `row`            | Default. Items go left to right |
| `row-reverse`    | Right to left                   |
| `column`         | Top to bottom                   |
| `column-reverse` | Bottom to top                   |

---

### 2️⃣ `justify-content` (Main Axis Alignment)

| Value           | Behavior                                 |
| --------------- | ---------------------------------------- |
| `flex-start`    | Items align at the start                 |
| `flex-end`      | Items align at the end                   |
| `center`        | Items are centered                       |
| `space-between` | Items spread out, first and last at ends |
| `space-around`  | Equal space around each item             |
| `space-evenly`  | Equal space between and around           |

---

### 3️⃣ `align-items` (Cross Axis Alignment)

| Value        | Description                              |
| ------------ | ---------------------------------------- |
| `stretch`    | Default, items stretch to fill container |
| `flex-start` | Align to top (in row direction)          |
| `flex-end`   | Align to bottom                          |
| `center`     | Vertically center                        |
| `baseline`   | Align based on text baseline             |

---

## 🧪 Practice for Part 1

Let students:

* Change `flex-direction` to `column`
* Try different `justify-content` and `align-items` values
* Observe changes by resizing browser window

---

# 🎓 **Flexbox Tutorial - Part 2: Advanced Flexbox**

## 📘 Part 2 Topics:

### 5. `flex-wrap`

### 6. `align-content`

### 7. `gap`

### 8. Individual Item Properties:

* `flex-grow`
* `flex-shrink`
* `flex-basis`
* `order`
* `align-self`

---

## 🧪 Example Code (Part 2)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Flexbox Part 2</title>
  <style>
    .container {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      border: 2px solid #ccc;
      padding: 10px;
    }

    .box {
      flex: 1 1 100px; /* grow, shrink, basis */
      height: 100px;
      background-color: #e74c3c;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .box:nth-child(3) {
      order: -1; /* comes first */
      background-color: #2ecc71;
    }

    .box:nth-child(4) {
      align-self: flex-end;
      background-color: #f39c12;
    }
  </style>
</head>
<body>

  <h2>Flexbox Part 2: Advanced Properties</h2>

  <div class="container">
    <div class="box">1</div>
    <div class="box">2</div>
    <div class="box">3 (order: -1)</div>
    <div class="box">4 (align-self: end)</div>
  </div>

</body>
</html>
```

---

## 🔍 Explanation of Advanced Properties

### 🔁 `flex-wrap`

* Allows items to wrap to the next line
* Values: `nowrap` (default), `wrap`, `wrap-reverse`

### 🧱 `flex-grow`, `flex-shrink`, `flex-basis`

Shorthand:

```css
flex: 1 1 100px;
```

* `flex-grow`: how much the item can grow
* `flex-shrink`: how much it can shrink
* `flex-basis`: starting size before growing/shrinking

### 🔢 `order`

* Controls the display order
* Lower value = appears earlier

### 🎯 `align-self`

* Overrides `align-items` for individual item

---

## 🧪 Practice for Part 2

* Change `flex-basis` to `150px`
* Set `flex-wrap: wrap` and reduce container width
* Try `order` values to rearrange items
* Use `align-self` on different items

---

## ✅ Summary

| Property          | Use                     |
| ----------------- | ----------------------- |
| `flex-direction`  | Row or column layout    |
| `justify-content` | Main-axis alignment     |
| `align-items`     | Cross-axis alignment    |
| `flex-wrap`       | Wrap items to next line |
| `gap`             | Space between items     |
| `flex-grow`       | Proportional growth     |
| `order`           | Change item order       |
| `align-self`      | Individual alignment    |