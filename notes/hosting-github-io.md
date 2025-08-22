## Guide to deploy a static website using GitHub Pages (on `github.io`) from a GitHub repo

---

### ✅ **Prerequisites**

- A GitHub account
- A Git repository with your static website files (`index.html`, `style.css`, etc.)

---

### 🚀 **Steps to Deploy:**

#### **1. Push your static site to a GitHub repo**

Make sure your site files are in a GitHub repository.

You can use this structure:

```
my-website/
├── index.html
├── style.css
└── images/
```

---

#### **2. Go to GitHub > Your Repository > Settings**

1. Click on the **⚙️ "Settings"** tab of your repository.
2. Scroll down to **"Pages"** (left sidebar).

---

#### **3. Configure GitHub Pages**

1. Under **"Source"**, choose the branch to publish from (usually `main` or `master`).
2. Select the folder:

   - If your files are in the root: choose `/ (root)`
   - If in a `docs/` folder: choose `/docs`

3. Click **"Save"**

---

#### **4. Wait for a few seconds...**

GitHub will build and deploy your site.

---

#### **5. Access your site**

It will be live at:

```
https://<your-username>.github.io/<repo-name>/
```

Example:

```
https://rahuldev.github.io/portfolio/
```

---

### 💡 Tips:

- Your `index.html` must be in the selected folder (`root` or `/docs`).
- You can update your site anytime by pushing new commits to the repo.