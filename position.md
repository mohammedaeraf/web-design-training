# 🎓 CSS Positioning – Complete Tutorial with Examples

---

## 📘 What is `position` in CSS?

The `position` property in CSS is used to control how an element is placed in the document. It determines the positioning context and how top/right/bottom/left values behave.

---

## 🧭 Position Types

### 1. `static` (default)

```css
position: static;
```

* This is the **default** value for all elements.
* The element flows **naturally** in the page layout.
* `top`, `right`, `bottom`, and `left` have **no effect**.

✅ **When to use?**
When you don’t need custom positioning. Most elements are static unless changed.

---

### 2. `relative`

```css
position: relative;
top: 10px;
left: 20px;
```

* The element stays **in its original place**, but can be **moved relative to itself**.
* Space for the element is still reserved in the layout.

✅ **Use for:**
Slight adjustments or to act as a **container for absolutely positioned children**.

### 🔸 Example

```html
<div style="position: relative; top: 20px; left: 30px;">I'm moved relative to my original position.</div>
```

---

### 3. `absolute`

```css
position: absolute;
top: 10px;
right: 20px;
```

* The element is removed from the normal flow.
* Positioned **relative to the nearest positioned ancestor** (not static).
* If none found, it is positioned relative to the `<html>` element.

✅ **Use for:**
Tooltips, popups, dropdowns, badges.

### 🔸 Example

```html
<div style="position: relative; width: 300px;">
  <div style="position: absolute; top: 10px; right: 10px;">Badge</div>
</div>
```

---

### 4. `fixed`

```css
position: fixed;
top: 0;
right: 0;
```

* The element is positioned **relative to the viewport** (browser window).
* It stays fixed **even while scrolling**.

✅ **Use for:**
Sticky headers, floating buttons, back-to-top links.

### 🔸 Example

```html
<div style="position: fixed; bottom: 20px; right: 20px;">Help</div>
```

---

### 5. `sticky`

```css
position: sticky;
top: 0;
```

* Acts like `relative` until it reaches a scroll threshold, then becomes `fixed`.
* Must define `top`, `left`, or `right`.

✅ **Use for:**
Sticky navbars, sticky headings in tables, etc.

### 🔸 Example

```html
<nav style="position: sticky; top: 0;">Sticky Navbar</nav>
```

---

## 🧪 Comparison Table

| Type       | Scrolls with Page | Stays in Flow | Relative To                     |
| ---------- | ----------------- | ------------- | ------------------------------- |
| `static`   | ✅ Yes             | ✅ Yes         | Normal document flow            |
| `relative` | ✅ Yes             | ✅ Yes         | Itself                          |
| `absolute` | ❌ No              | ❌ No          | Nearest positioned parent       |
| `fixed`    | ❌ No              | ❌ No          | Viewport                        |
| `sticky`   | ✅ / ❌ Partial     | ✅ Yes         | Scroll position (then viewport) |

---

## 🧠 Tips for Teaching

* Start with static, then show small `relative` shifts.
* Explain **positioning context** when using `absolute`.
* Demo sticky headers or fixed buttons with a scrollable page.

---

## 🧑‍💻 Assignment Idea

**Create a Contact Page** with:

* A fixed “Help” button at bottom right
* A sticky navbar
* A profile badge using `absolute` inside a card

