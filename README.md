# 🏔️ The Night Road Trip — Personal Portfolio Guide

Welcome to your personal portfolio! This website was engineered specifically for a B.Tech Computer Science student and traveller who loves mountain passes and driving.

It is built **100% strictly with plain HTML and CSS**.
- **Zero JavaScript** (no scripts to break, debug, or load).
- **Zero Node/npm, zero build tools, zero dependencies**.
- Works immediately by simply **double-clicking `index.html`** in any web browser on Mac, Windows, or Linux.

---

## 🗂️ File Tour & Structure

```
portfolio/
├── index.html          # Stop 1: Base Camp (Home, 3D Hero, Featured Expeditions, Marquee)
├── about.html          # Stop 2: The Traveller (Portrait with Mountain Mask, Bio, Trip Log)
├── projects.html       # Stop 3: Expeditions (RupeeWise, GatiSetu, CSS Filter Tabs, Modals)
├── skills.html         # Stop 4: Toolkit (Gear Panels, 3D Rotating Compass, Tachometer Meters)
├── education.html      # Stop 5: Milestones (Highway Signboards along a Road, Certifications)
├── interests.html      # Stop 6: Off-Road (Parallax Bands, Photo Galleries, Interactive Dark Map)
├── contact.html        # Stop 7: Summit (Night Aurora, HTML5 Contact Form, Social Buttons)
├── 404.html            # Off-Road Dead End ("Wrong turn. This road doesn't exist.")
├── css/
│   └── style.css       # The single master stylesheet shared by all pages
├── images/             # Folder for all your personal photos
│   └── README.txt      # Guide to image dimensions & drop-in names
└── README.md           # This beginner's handbook
```

---

## 1. How to Open & Test the Site

1. Open your computer's file explorer / Finder.
2. Locate the `portfolio` folder.
3. **Double-click `index.html`**.
4. The site will open right inside your default web browser (Chrome, Safari, Firefox, Edge, Brave, etc.).
5. Click around! Every link, loading animation, modal popup, filter tab, and gallery works right away offline.

---

## 2. How to Edit Text in Any File

Every single HTML file is organized with plain-English comments starting with `<!-- ✏️ EDIT: ... -->`.

1. Right-click any `.html` file (for example `index.html` or `about.html`) and choose **Open With** → **TextEdit**, **Notepad**, or your code editor like **VS Code**.
2. Press `Ctrl + F` (or `Cmd + F` on Mac) and search for:
   ```text
   ✏️ EDIT:
   ```
   or search for:
   ```text
   [PLACEHOLDER]
   ```
3. Type your personal details in place of the bracketed placeholders.
4. Save the file (`Ctrl + S` or `Cmd + S`) and refresh your browser!

---

## 3. Where to Put Your Photos

You do not need to edit complex CSS code to add your pictures. Just drop your image files directly into the `images/` folder with these exact names:

| File Name | Page Used On | Recommended Size | Description |
| :--- | :--- | :--- | :--- |
| **`profile.jpg`** | `about.html` | 800 × 1000 px | Your portrait (clipped with a mountain mask). |
| **`project-rupeewise.jpg`** | `index.html` & `projects.html` | 1200 × 750 px | Screenshot / mockup of RupeeWise Android app. |
| **`project-gatisetu.jpg`** | `index.html` & `projects.html` | 1200 × 750 px | Screenshot / logo of GatiSetu logistics portal. |
| **`project3.jpg`** | `projects.html` | 1200 × 750 px | Cover image for your 3rd project. |
| **`project4.jpg`** | `projects.html` | 1200 × 750 px | Cover image for your 4th project. |
| **`trek1.jpg`, `trek2.jpg`, `trek3.jpg`** | `interests.html` | 1200 × 800 px | Photos of mountain passes, peaks, and trekking trails. |
| **`drive1.jpg`, `drive2.jpg`, `drive3.jpg`** | `interests.html` | 1200 × 800 px | Photos of highways, car cockpit, or road trips. |
| **`trip1.jpg`, `trip2.jpg`, `trip3.jpg`** | `interests.html` | 1200 × 800 px | Photos of scenic landscapes, night sky, or camps. |

> **Note:** If you haven't taken all the photos yet, don't worry! The site has elegant dark-gradient and SVG blueprint placeholders built in, so it never looks broken even before photos are added.

---

## 4. How to Change Colors (The CSS Palette)

All colors are controlled in **one central place** at the very top of `css/style.css`:

```css
:root {
  /* Core Background & Surfaces */
  --bg: #07090C;             /* Deep asphalt night background */
  --surface: #0E1218;        /* Glass card base */
  --border: rgba(255, 255, 255, 0.08);

  /* Typography Colors */
  --text: #E8ECF1;           /* Crisp moonlight text */
  --muted: #8A94A3;          /* Foggy grey descriptions */

  /* Atmospheric Accent Colors */
  --amber: #FFB547;          /* Warm headlight amber glow */
  --orange: #FF7A2F;         /* Twilight horizon glow */
  --blue: #6FB7FF;           /* Mountain sky dusk blue */
}
```

Want a neon electric cyan or forest green accent? Just change `--amber: #FFB547;` to your preferred hex code (e.g. `--amber: #00E5FF;`), and the entire site (glows, headlights, progress bars, links) updates automatically!

---

## 5. How to Add a New Project Card

In `projects.html`, locate the copy-paste template comment. Paste this block inside `<div class="projects-grid">`:

```html
<article class="project-card" data-category="mobile">
  <div class="project-cover">
    <div class="project-cover-placeholder">
      <img src="images/my-new-project.jpg" alt="Cover" loading="lazy" onerror="this.style.display='none'">
      <div class="project-badge-top">
        <span class="tag-chip active">ANDROID // NEW</span>
      </div>
    </div>
  </div>
  <div class="project-body">
    <span class="project-category">Native Android</span>
    <h2 class="project-title">My Project Name</h2>
    <p class="project-summary">A short sentence explaining what you engineered.</p>
    <div class="project-tags">
      <span class="tag-chip">Kotlin</span>
      <span class="tag-chip">Jetpack Compose</span>
    </div>
    <div class="project-footer">
      <span>Status: Shipped</span>
      <a href="#modal-myproject" class="btn btn-secondary" style="padding: 0.5rem 1rem; font-size: 0.8125rem;">
        View Details →
      </a>
    </div>
  </div>
  <div class="project-route-line"></div>
</article>
```

Then at the bottom of `projects.html`, copy one of the `<div class="modal-overlay" id="...">` blocks, give it `id="modal-myproject"`, and write your full overview!

---

## 6. How to Change Skill Levels

In `skills.html`, each skill card has a gauge meter with a single inline CSS variable. Simply change the percentage number:

```html
<!-- Example: Changing Kotlin to 95% -->
<div class="skill-gauge-card">
  <div class="skill-meta">
    <span class="skill-name">Kotlin</span>
    <span class="skill-percent">95%</span> <!-- 1. Change text here -->
  </div>
  <div class="skill-track">
    <div class="skill-fill" style="--level: 95%;"></div> <!-- 2. Change variable here -->
  </div>
</div>
```

---

## 7. How to Set Up the Contact Form (Formspree)

On `contact.html`, the contact form sends dispatches directly to your personal email inbox using **Formspree** (a free service for static HTML websites):

1. Go to [https://formspree.io](https://formspree.io) and register with your email address for free.
2. Click **"+ New Form"** and name it "Portfolio Contact".
3. Formspree will give you an Endpoint URL like:
   `https://formspree.io/f/mqkvopzw` (where `mqkvopzw` is your Form ID).
4. Open `contact.html`, find line ~185, and update the form action:
   ```html
   <form action="https://formspree.io/f/mqkvopzw" method="POST" class="contact-form">
   ```
5. Save the file. When someone submits the form, you will receive an instant email!

---

## 8. How to Put Your Site Online for Free

### Option A: Netlify Drop (Fastest — 30 seconds)
1. Go to [https://app.netlify.com/drop](https://app.netlify.com/drop) (free account).
2. Simply **drag and drop your entire `portfolio/` folder** into the circle in your browser.
3. Your site is live instantly with a free `.netlify.app` web address and free HTTPS!

### Option B: GitHub Pages (Recommended for Developers)
1. Create a free account at [https://github.com](https://github.com).
2. Create a new repository named `portfolio` (or `yourusername.github.io`).
3. Upload all files from your `portfolio/` folder into this repository.
4. Go to repository **Settings** → **Pages** (on the left sidebar).
5. Under **Branch**, select `main` (root) and click **Save**.
6. Within 1 minute, your portfolio will be live at `https://yourusername.github.io/portfolio/`!

---

## 9. Complete Placeholder Checklist

Before publishing, search for these bracketed terms in your code editor and fill in your details:

- [ ] **Your Name & Initials:** Replace `[YOUR NAME]` and `[TP]` across all `.html` files.
- [ ] **Resume:** Put your PDF file named `resume.pdf` in the root `portfolio/` folder.
- [ ] **Location:** Replace `[GUJARAT / INDIA]` or `[CITY, INDIA]` in `about.html` and `contact.html`.
- [ ] **Email:** Replace `[YOUR_EMAIL@EXAMPLE.COM]` in `about.html` and `contact.html`.
- [ ] **College/University:** Replace `[COLLEGE NAME, AFFILIATED UNIVERSITY]` in `about.html` and `education.html`.
- [ ] **Education Scores:** Replace `[X.XX / 10.0]` CGPA and 10th/12th percentages `[XX.X%]` in `education.html`.
- [ ] **RupeeWise URLs:** Replace `[YOUR_GITHUB_RUPEEWISE_URL]` and `[YOUR_DEMO_RUPEEWISE_URL]` in `projects.html`.
- [ ] **GatiSetu URLs:** Replace `[YOUR_GATISETU_PORTAL_URL]` and `[YOUR_GATISETU_GITHUB_URL]` in `projects.html`.
- [ ] **Social Profiles:** Replace `[YOUR_GITHUB_URL]`, `[YOUR_LINKEDIN_URL]`, `[YOUR_X_TWITTER_URL]`, and `[YOUR_INSTAGRAM_URL]` in `contact.html`.
- [ ] **Formspree ID:** Replace `[YOUR_FORM_ID]` in `contact.html`.
- [ ] **Cockpit Notes:** Put your favourite car, dream drive, and favourite trek/peak in `interests.html`.
- [ ] **Photos:** Drop your photos into `images/` (see section 3 above).

---

*Safe travels on the road and in your engineering journey!*
