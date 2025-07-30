# 🎓 CSS Units Tutorial

**Understanding px, em, rem, %, and Making Circular Images**

---

## 🔹 What Are CSS Units?

CSS units define **measurements** for elements like width, height, font-size, margin, padding, and more.

They are categorized into:

| Unit Type    | Examples                     |
| ------------ | ---------------------------- |
| **Absolute** | `px`, `pt`, `cm`, `in`       |
| **Relative** | `em`, `rem`, `%`, `vw`, `vh` |

We'll focus on the most commonly used: `px`, `em`, `rem`, `%`

---

## ✅ 1. `px` — Pixels

* Fixed, absolute value.
* Doesn't scale automatically.
* Common for borders, icons, or when exact sizing is needed.

```css
width: 200px;
font-size: 16px;
```

---

## ✅ 2. `em` — Relative to Parent Font Size

* 1em = size of the parent’s font.
* Inherits and **multiplies** through nesting.

```css
font-size: 1.5em; /* 1.5 × parent font size */
```

---

## ✅ 3. `rem` — Relative to Root (`html`) Font Size

* Consistent across the page.
* Easier to manage for responsive design.

```css
:root {
  font-size: 16px;
}

font-size: 2rem; /* 32px */
```

---

## ✅ 4. `%` — Relative to Parent Element's Size

* Used in widths, heights, margins.
* Often used in responsive design.

```css
width: 80%; /* 80% of parent width */
```

---

## 💡 Code Sample: Demonstrating `px`, `em`, `rem`, %

### 📄 `units-demo.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>CSS Units Demo</title>
  <style>
    :root {
      font-size: 16px; /* 1rem = 16px */
    }

    body {
      font-family: Arial, sans-serif;
      padding: 20px;
    }

    .px-box {
      width: 200px;
      height: 100px;
      background-color: #f0a;
      margin-bottom: 15px;
    }

    .em-box {
      font-size: 1.5em;  /* relative to body */
      padding: 1em;
      background-color: #0af;
      width: 20em;
      margin-bottom: 15px;
    }

    .rem-box {
      font-size: 1.2rem; /* 1.2 × root font size */
      padding: 1rem;
      background-color: #afa;
      width: 25rem;
      margin-bottom: 15px;
    }

    .container {
      width: 400px;
      padding: 10px;
      background-color: #f9f9f9;
      border: 1px solid #ccc;
    }

    .percent-box {
      width: 80%;
      height: 50px;
      background-color: #ffa500;
    }

    h2 {
      font-size: 1.5rem;
    }
  </style>
</head>
<body>

  <h2>CSS Units Demonstration</h2>

  <div class="px-box">Fixed size using <strong>px</strong> (200px width)</div>

  <div class="em-box">Relative size using <strong>em</strong> (1.5em font size)</div>

  <div class="rem-box">Relative size using <strong>rem</strong> (1.2rem font size)</div>

  <div class="container">
    <div class="percent-box">Width set to <strong>80%</strong> of container (400px)</div>
  </div>

</body>
</html>
```

---

## 🎯 Bonus: Make an Image Circular with `border-radius`

Use `border-radius: 50%` on a square image to create a **perfect circle**.

### 📄 `round-image.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Round Image Example</title>
  <style>
    .round-image {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      object-fit: cover;
    }
  </style>
</head>
<body>

  <h2>My Profile Picture</h2>
  <img src="https://via.placeholder.com/150" alt="Profile" class="round-image" />

</body>
</html>
```

---

## 🧠 Summary Table

| Unit  | Relative To              | Common Use                |
| ----- | ------------------------ | ------------------------- |
| `px`  | Absolute (device pixels) | Fixed sizes               |
| `em`  | Parent font size         | Spacing, scaling text     |
| `rem` | Root (`html`) font size  | Consistent layout & text  |
| `%`   | Parent element’s size    | Responsive widths/heights |

---

## 🔹 `em` vs `rem`

| Feature              | `em`                                             | `rem`                                          |
| -------------------- | ------------------------------------------------ | ---------------------------------------------- |
| **Full Form**        | "element-relative unit"                          | "root element-relative unit"                   |
| **Relative To**      | The **font size of the parent element**          | The **font size of the root (`html`) element** |
| **Cascading Effect** | Yes — `em` values **accumulate** through nesting | No — always consistent across the page         |
| **Use Case**         | For padding/margin relative to element size      | For consistent font sizing across the site     |
| **Behavior**         | Inherits and **multiplies** with each level      | Stays consistent no matter where it's used     |

---

## 🧪 Example to Compare

### 💡 CSS

```css
html {
  font-size: 16px;  /* 1rem = 16px */
}

.container {
  font-size: 20px;
}

.em-example {
  font-size: 2em;   /* 2 * 20px = 40px */
}

.rem-example {
  font-size: 2rem;  /* 2 * 16px = 32px */
}
```

### 🧾 Explanation:

* `.em-example` → `2em` → relative to `.container` (20px) → becomes **40px**
* `.rem-example` → `2rem` → relative to `html` (16px) → becomes **32px**

---

## 🔧 When to Use

| Use `em` when…                                  | Use `rem` when…                                |
| ----------------------------------------------- | ---------------------------------------------- |
| You want spacing to scale with parent font size | You want **uniform sizing** across entire site |
| Creating components with scalable padding       | Setting global font sizes or modular scale     |

---

## 🚫 Common Pitfall with `em`:

Nested `em` units can multiply unexpectedly:

```css
.container { font-size: 1.2em; }     /* 1.2 × 16 = 19.2px */
.child     { font-size: 1.2em; }     /* 1.2 × 19.2 = 23.04px */
```

✅ Use `rem` to **avoid compounding** like this.
