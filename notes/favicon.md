## 🧑‍🏫 **Adding a Favicon to Your Website**

### ✅ What is a Favicon?

A **favicon** (short for “favorite icon”) is the small icon that appears in the browser tab, bookmarks, and history next to the page title.

![Example Favicon](https://upload.wikimedia.org/wikipedia/commons/3/31/Google_favicon_2015.png)

---

## 🛠️ Steps to Add a Favicon

### 📁 1. Prepare the Favicon File

- Format: `.ico`, `.png`, `.svg` (most modern browsers support `.png`)
- Size: Ideally `32x32` or `16x16` pixels
- Name it: `favicon.ico` or `favicon.png`

---

### 📄 2. Place the File in Your Project Folder

For example:

```
project-folder/
├── index.html
└── favicon.png
```

---

### 🧾 3. Add Link to Favicon in HTML `<head>`

Add this inside the `<head>` section of your HTML file:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Favicon Demo</title>

    <!-- Add Favicon -->
    <link rel="icon" type="image/png" href="favicon.png" />
  </head>
  <body>
    <h1>Welcome to My Website</h1>
    <p>This page has a favicon!</p>
  </body>
</html>
```

---

## 🔁 Refresh Your Browser

- Save the file.
- Refresh the page.
- You might need to **clear cache** or open in **incognito mode** to see the new favicon.

---

## 🔍 Common Mistakes

| Mistake        | Fix                      |
| -------------- | ------------------------ |
| File not found | Check file name and path |
| Wrong format   | Use `.png` or `.ico`     |
| No change      | Clear browser cache      |
