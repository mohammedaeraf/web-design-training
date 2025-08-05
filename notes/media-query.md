# 🎓 CSS Media Queries Tutorial

### Make Your Website Responsive with Simple Examples

---

## 📌 What is a Media Query?

A **Media Query** in CSS allows you to apply styles **only when certain conditions are met** — such as screen width, height, device type, or orientation.

It helps you create **responsive designs** that work well on all devices (mobile, tablet, desktop).

---

## ✅ Syntax

```css
@media (condition) {
  /* CSS rules for that condition */
}
```

Example:

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

🧠 Meaning: If the screen is **600px or less**, change the background to light blue.

---

## 📄 Demo 1: Change Background on Mobile

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Media Query Demo</title>
  <style>
    body {
      background-color: #ffffff;
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 20px;
    }

    @media (max-width: 600px) {
      body {
        background-color: #dff9fb;
      }
    }
  </style>
</head>
<body>

  <h2>Resize the browser to see background change</h2>

</body>
</html>
```

---

## 📄 Demo 2: Responsive Box Layout

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Responsive Boxes</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: #00b894;
      margin: 10px;
      display: inline-block;
    }

    @media (max-width: 600px) {
      .box {
        display: block;
        margin: 10px auto;
      }
    }
  </style>
</head>
<body>

  <h2>Responsive Boxes</h2>
  <div class="box"></div>
  <div class="box"></div>
  <div class="box"></div>

</body>
</html>
```

🧠 On screens wider than 600px, boxes appear **side by side**.
On small screens, they appear **stacked**.
