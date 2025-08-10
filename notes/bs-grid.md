# 📚 Tutorial: Bootstrap Grid System

## 1️⃣ What is the Bootstrap Grid System?

The **Bootstrap Grid System** is a **flexbox-based** layout system that helps you create responsive designs easily.
It works by dividing the page into **12 equal columns**, and you place your content inside these columns.
You can combine columns to take up more space or make them adjust automatically for different screen sizes.

---

## 2️⃣ How It Works

* The **grid** uses a **container** to center and pad the content.
* **Rows** are used to group columns horizontally.
* **Columns** contain your actual content.
* The width of each column is defined using `.col-*` classes.

---

## 3️⃣ Bootstrap Grid Classes for Screen Sizes

| Class Prefix | Screen Size | Min Width |
| ------------ | ----------- | --------- |
| `.col-`      | Extra Small | <576px    |
| `.col-sm-`   | Small       | ≥576px    |
| `.col-md-`   | Medium      | ≥768px    |
| `.col-lg-`   | Large       | ≥992px    |
| `.col-xl-`   | Extra Large | ≥1200px   |
| `.col-xxl-`  | XXL         | ≥1400px   |

---

## 4️⃣ Basic Structure

```html
<div class="container">
  <div class="row">
    <div class="col">Column 1</div>
    <div class="col">Column 2</div>
    <div class="col">Column 3</div>
  </div>
</div>
```

---

## 5️⃣ Example: Equal Columns

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bootstrap Grid Example</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<div class="container mt-4">
  <h2 class="mb-4">Bootstrap Grid System - Equal Columns</h2>
  
  <div class="row">
    <div class="col bg-primary text-white p-3">Column 1</div>
    <div class="col bg-success text-white p-3">Column 2</div>
    <div class="col bg-warning text-dark p-3">Column 3</div>
  </div>
</div>

</body>
</html>
```

💡 Here, `.col` automatically divides the space equally between columns.

---

## 6️⃣ Example: Different Column Sizes

```html
<div class="container mt-4">
  <h2>Different Column Sizes</h2>
  <div class="row">
    <div class="col-4 bg-info text-white p-3">Takes 4/12 columns</div>
    <div class="col-8 bg-dark text-white p-3">Takes 8/12 columns</div>
  </div>
</div>
```

💡 Columns always add up to **12** for a row.

---

## 7️⃣ Example: Responsive Columns

```html
<div class="container mt-4">
  <h2>Responsive Columns</h2>
  <div class="row">
    <div class="col-sm-6 col-lg-4 bg-primary text-white p-3">Column A</div>
    <div class="col-sm-6 col-lg-4 bg-success text-white p-3">Column B</div>
    <div class="col-sm-12 col-lg-4 bg-warning text-dark p-3">Column C</div>
  </div>
</div>
```

💡 On small screens, columns stack; on large screens, they sit side by side.

---

## 8️⃣ Key Tips for Students

* Always wrap rows inside a `.container` or `.container-fluid`.
* A row must be inside a container.
* Columns should always be inside rows.
* Use `.col` for equal-width columns or `.col-*` for fixed widths.
* Use responsive classes (`col-sm-*`, `col-md-*`, etc.) to make layouts adjust on different devices.
