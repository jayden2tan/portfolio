# Personal Portfolio Website - Jayden Tan

A beautiful, modern, and handcrafted personal portfolio website designed for high school students to showcase their work, skills, and experience for college applications or internships.

Everything is completely self-contained within a single file: `index.html`. There are no complicated servers to set up, packages to install, or command line tools required.

---

## 🚀 Getting Started

### 1. Open the Website Locally
- Ensure the `index.html` file is in your local directory.
- **Double-click `index.html`**. It will instantly open in your default web browser (Chrome, Edge, Firefox, Safari).
- To make changes, you need to open `index.html` in a text editor. We recommend downloading [VS Code](https://code.visualstudio.com/) (free and highly recommended), or you can use standard editors like Notepad (Windows) or TextEdit (Mac).

---

## 🎨 How to Customize

All areas that can be customized are marked with an `[EDIT]` comment in the code to make searching easy. Open `index.html` in your text editor and use the search shortcut (**Ctrl + F** on Windows or **Cmd + F** on Mac) to locate `[EDIT]`.

### 2. Edit Text Content & Links
Search for `[EDIT]` and replace the placeholder text directly inside the tags with your personal details:
```html
<!-- Example of text edit -->
<h1 class="hero-title heading-xl">
  Hi, I'm <span class="accent-text">[EDIT] Jayden Tan</span>
</h1>
```

### 3. Replace the Monogram with a Profile Photo
By default, the website displays your initials `JT` as a professional initials monogram. When you want to replace it with a profile picture:
1. Copy your photo (e.g. `me.jpg`) into the **same folder** as `index.html`.
2. Open `index.html` and search for the comment `Avatar container`.
3. Locate this code:
   ```html
   <div class="avatar-container" id="avatar-container">
     <span class="avatar-fallback" id="avatar-fallback">JT</span>
   </div>
   ```
4. Replace it with:
   ```html
   <div class="avatar-container" id="avatar-container">
     <img class="avatar" src="me.jpg" alt="Jayden Tan Profile Picture">
   </div>
   ```
5. Save the file and refresh your browser.

### 4. Customizing the Accent Preset Colors
The website comes with a dynamic accent color picker containing 5 swatches in the top right. You can modify these presets in the CSS `:root` block:
```css
/* Locate under DESIGN SYSTEM & CSS VARIABLES */
--accent-blue: #3b82f6;
--accent-emerald: #10b981;
--accent-violet: #8b5cf6;
--accent-rose: #f43f5e;
--accent-amber: #f59e0b;
```
If you change these, make sure to also update the corresponding Hex color codes in BOTH the `data-color` and `style` attributes on the picker buttons in the HTML:
```html
<!-- Locate under Preset Swatches Accent Color Picker -->
<button class="swatch-btn" data-color="#10b981" style="background-color: #10b981;" ...></button>
```

---

## 🌐 How to Publish Online (Free)

Once you are done customizing the site locally, you can publish it online for free so you can link it on your resume, LinkedIn, or college application form.

### Option A: Netlify Drop (Easiest, takes 1 minute)
1. Go to [Netlify Drop](https://app.netlify.com/drop).
2. Drag and drop the **entire folder** containing your `index.html` (and your photo if you added one).
3. Netlify will generate a temporary URL (e.g., `https://random-name.netlify.app`).
4. You can sign up for a free Netlify account to change this to a custom address (e.g., `https://jaydentan.netlify.app`) or update your site by dragging the folder again.

### Option B: GitHub Pages (Recommended for Resumes)
Using GitHub is ideal for demonstrating technical proficiency on internships.
1. Sign up for a free account on [GitHub](https://github.com).
2. Create a new repository named exactly: `yourusername.github.io` (replace `yourusername` with your actual GitHub username).
3. Set the repository visibility to **Public**.
4. Click **Upload an existing file** and drag in your `index.html` (and your profile image if you have one). Commit the changes.
5. In your repository, go to **Settings** $\rightarrow$ **Pages** (on the left menu).
6. Under "Build and deployment", select **Deploy from a branch** and change the branch selection to **main**. Click **Save**.
7. Wait 1-2 minutes. Your site will be live at: `https://yourusername.github.io`

---

## 🔍 Troubleshooting

- **My changes aren't appearing in the browser:**
  - Make sure you saved the file in your text editor (**Ctrl + S** or **Cmd + S**).
  - Refresh the browser tab. If it still doesn't update, try a "hard refresh" (**Ctrl + Shift + R** on Windows or **Cmd + Shift + R** on Mac) to bypass cached files.
- **The custom fonts look generic or don't display:**
  - The Space Grotesk and Inter fonts load from the internet via Google Fonts. If you are offline, the website uses system fallbacks. Reconnect to the internet and reload the page.
- **My profile image is broken:**
  - Ensure the image file is in the *same folder* as `index.html`.
  - Check spelling and file extension. Note that filenames are case-sensitive (`me.jpg` is different from `me.JPG` or `me.png`).
