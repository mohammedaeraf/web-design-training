# 🎓 Tutorial: CSS Variables (Custom Properties)

## 🧾 What are CSS Variables?

CSS Variables allow you to **store values** (like colors, sizes, spacing) in a reusable way.
They make your CSS:

* Easier to read
* Easier to update
* More consistent

---

## ✅ Syntax

```css
--custom-name: value;
```

* Defined inside a selector (usually `:root`)
* Accessed using `var(--custom-name)`

---

## 📄 Example: Basic CSS Variable Demo

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>CSS Variables Demo</title>
  <style>
    :root {
      --main-color: #3498db;
      --text-color: white;
      --padding: 10px;
      --border-radius: 8px;
    }

    .box {
      background-color: var(--main-color);
      color: var(--text-color);
      padding: var(--padding);
      border-radius: var(--border-radius);
    }
  </style>
</head>
<body>

  <div class="box">This box uses CSS Variables!</div>

</body>
</html>
```

---

## 🧠 Why Use CSS Variables?

| Without Variables     | With Variables                |
| --------------------- | ----------------------------- |
| `color: #3498db;`     | `color: var(--main-color);`   |
| Update in many places | Update in one place (`:root`) |
| Repetition            | Reusability                   |
| Hard to maintain      | Easier to maintain            |

---

## 🌐 Where to Declare CSS Variables?

### Global (recommended)

```css
:root {
  --main-color: #e74c3c;
}
```

### Inside a class (local scope)

```css
.card {
  --main-color: #2ecc71;
}
```

---

## 🧪 Practice Activity

Ask students to:

1. Create 2 boxes using the same variables.
2. Change the variable values in `:root` and observe the effect on both boxes.
3. Add a `hover` effect that uses a different variable.

---

## 🚀 Bonus: Fallback Values

You can give a fallback if the variable is not defined:

```css
background-color: var(--bg, #cccccc);
```

---

## 📌 Summary

| Feature             | Benefit                        |
| ------------------- | ------------------------------ |
| Reusability         | Define once, use many times    |
| Maintainability     | Easy updates from one location |
| Scoping             | Can be global or local         |
| Responsive Friendly | Combine with media queries     |