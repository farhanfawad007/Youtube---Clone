<div align="center">

# ▶️ YouTube Clone — Front-End Video Discovery & Watch Platform

<p align="center">
  <strong>A modular, responsive YouTube-inspired front-end web application built with Vanilla HTML5, CSS3, and ES6+ JavaScript.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/LocalStorage-State_Persistence-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="LocalStorage" />
</p>

</div>

---

## 📖 Project Overview

**YouTube Clone** is a lightweight, client-side media browsing and viewing web application crafted with semantic HTML5, custom CSS variables, and modular Vanilla JavaScript—requiring zero frameworks or external build tools. It replicates core YouTube workflows including a searchable thumbnail grid, category pill filtering, sidebar feed navigation (*Subscriptions*, *Saved*, *Liked*), custom local image uploading, an interactive Watch page with *Like / Save / Subscribe* actions and editable descriptions, demo authentication with one-click credential auto-fill, and persistent Dark/Light theming via `localStorage`.

---

## ✨ Key Features

### 🏠 Home Feed & Discovery (`index.html`)
* **Responsive Thumbnail Grid:** Dynamically renders video cards with result count metadata (`#resultsMeta`) and clean panel layouts.
* **Real-Time Search & Category Pills:** Filter content by keyword via the top search bar (`#searchInput`) or toggle category pills (*All*, *Entertainment*) with accessible `aria-pressed` states.
* **Hash-Based Sidebar Navigation:** Quick-access navigation panel for **Home**, **Trending** *(demo)*, **Subscriptions**, **Library** *(demo)*, **Saved**, and **Liked** collections.
* **Custom Image Uploader:** Upload multiple local images directly from your device (**Add Images** / `#imagePicker`) to populate custom feed items, or reset uploaded media anytime (**Clear Images**).

### 🎬 Interactive Watch Page (`watch.html`)
* **Two-Column Theater Layout:** Dedicated `1.6fr / 0.9fr` split view featuring the main media viewer (`#viewer`), video title, channel avatar, channel name, and view stats alongside an **Up next** recommendation queue (`#upNext`).
* **Engagement Controls:** Interactive **Like**, **Save**, and **Subscribe** buttons synced with client-side storage so liked/saved items and channel subscriptions persist across views.
* **Inline Description Editor:** View video descriptions in a styled panel (`#desc`) and update them on the fly using the built-in **Edit** button (`#editDescBtn`).

### 🔐 Demo Authentication (`login.html`)
* **Split Hero & Sign-In UI:** Modern two-panel authentication screen showcasing platform feature chips alongside a clean login card.
* **One-Click Demo Auto-Fill:** Includes a **Use demo** button (`#fillDemo`) that automatically populates valid test credentials for instant testing.
* **Session Management:** Stores login state in `localStorage` with instant **Logout** controls (`#logoutBtn`) available across both Home and Watch headers.

### 🌓 Theme Engine & Accessibility
* **Dark / Light Mode Toggle:** Defaults to sleek YouTube Dark Mode (`data-theme="dark"`) with a persistent **Theme** switcher (`#themeToggle`) across all pages, including the login screen.
* **Accessible Toast Notifications:** Live status feedback (`role="status"`, `aria-live="polite"`) for user actions, uploads, and authentication events.

---

## 🗂️ Project Architecture & File Structure

```text
youtube-clone/
├── assets/
│   └── logo.svg            # YouTube brand vector logo
├── scripts/
│   ├── storage.js          # LocalStorage wrapper & state persistence helpers
│   ├── theme.js            # Dark / Light mode toggle & data-theme sync
│   ├── auth.js             # Session guard, login verification, & logout handler
│   ├── data.js             # Seed video catalog, metadata, & channel data
│   ├── app.js              # Home grid rendering, search, pill filters, & sidebar routing
│   ├── uploader.js         # Multi-file local image picker & custom thumbnail management
│   ├── login.js            # Login form submission & "Use demo" auto-fill handler
│   └── watch.js            # Watch viewer, Like/Save/Subscribe toggles, description edit, & Up Next
├── styles/
│   ├── base.css            # Global design tokens, topbar, grid, sidebar, panels, & toast styles
│   └── auth.css            # Split-panel authentication layout & feature chip styles
├── index.html              # Main home feed, category pillbar, sidebar, & image uploader
├── login.html              # Demo sign-in portal with one-click credential auto-fill
├── watch.html              # Media watch view, engagement actions, & Up Next sidebar
└── README.md               # Project documentation
```

---

## 🧠 Client-Side Persistence (`localStorage`)

All user interactions run entirely in the browser and persist across page refreshes via `./scripts/storage.js`:

| Feature | Persisted Data |
| :--- | :--- |
| **Authentication** | Active demo user session state (`login.html` ↔ `index.html` / `watch.html`) |
| **Theme Preference** | Selected `dark` or `light` theme applied via `<html data-theme="...">` |
| **Engagement State** | Liked videos (`#liked`), Saved videos (`#saved`), and Channel Subscriptions (`#subscriptions`) |
| **Custom Media & Edits** | User-uploaded local images and edited video descriptions |

---

## 🚀 Getting Started

No `npm install` or backend server setup is required.

### 1. Clone the Repository
```bash
git clone [https://github.com/farhanfawad007/youtube-clone.git](https://github.com/farhanfawad007/youtube-clone.git)
cd youtube-clone
```

### 2. Run Locally
* **Option A — VS Code Live Server (Recommended):** Open the folder in VS Code, right-click `login.html` or `index.html`, and click **Open with Live Server**.
* **Option B — Local HTTP Server:**
  ```bash
  python -m http.server 5500
  ```
  Then visit `http://localhost:5500` in your browser.
* **Option C — Direct Launch:** Open `login.html` or `index.html` directly in any modern web browser.

---

## 🔑 Demo Login Credentials

Use the credentials below on `login.html` (or click the **Use demo** button to auto-fill them instantly):

| Field | Value |
| :--- | :--- |
| **Email** | `farhanfawad@gmail.com` |
| **Password** | `1234567` |

---

## 🔮 Future Enhancements

* HTML5 `<video>` playback integration alongside custom image thumbnails.
* Interactive comments section with timestamped user replies on `watch.html`.
* Additional category pills (*Music*, *Gaming*, *Tech*, *Coding*) and watch-history tracking under *Library*.
* IndexedDB storage upgrade to support larger local image and video file uploads.

---

## 👨‍💻 Author

**Syed Farhan Fawad**
* **GitHub:** [@farhanfawad007](https://github.com/farhanfawad007)
* **LinkedIn:** [Syed Farhan Fawad](https://linkedin.com/in/syed-farhan-fawad)

---

<div align="center">
  <sub>Built with ❤️ using Vanilla HTML, CSS & JavaScript</sub>
</div>
