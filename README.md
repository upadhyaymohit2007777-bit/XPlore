# 🚀 XPlore — Modern Student Micro-Learning & Telemetry Platform

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![GitHub Repository](https://img.shields.io/badge/GitHub-XPlore-blue?logo=github)](https://github.com/upadhyaymohit2007777-bit/XPlore)

**XPlore** is an interactive, gamified micro-learning web application and faculty telemetry portal designed for students and educators. It combines gamified learning mechanics (daily interactive quizzes, dynamic XP, streak tracking, and achievement badges) with a faculty Content Management System (CMS) that delivers real-time student telemetry, quiz authoring, and course curriculum distribution.

---

## 👥 Project Team

Project developed by:
- **Vivek Kumar**
- **Mohit Upadhyay**
- **Lalit Choudhary**
- **Yashasvi Sarswat**

---

## 🌟 Key Features

### 🎓 1. Student Learning Portal (`index.html`)
- **Dashboard & Leaderboards**: Live student rankings, contest leaderboards, global statistics, and weekly performance analytics.
- **Daily Micro-Learning & Quizzes**: Engaging, timed interactive quiz modules with dynamic XP awards, instant answer feedback, and synthesized Web Audio sound effects.
- **Milestone Rewards & Badges**: Interactive badge inspection modals (e.g., *First Steps*, *Rising Star*), day-streak activity tracking, and achievements.
- **Student Space & Profile**: Personal study metrics, avatar customization, dynamic system clock, audio synthesizer toggles, and session persistence.
- **Responsive Mobile-First UI**: Bottom tab navigation bar (`Overview`, `Today`, `Rewards`, `Profile`) designed with sleek dark-mode glassmorphism and Apple-inspired typography.

### 🛠️ 2. Faculty CMS & Telemetry Console (`cms.html`)
- **Telemetry & Student Monitoring**: Real-time analytics displaying active learner counts, average completion rates, XP distribution across cohorts, and automated low-engagement warnings.
- **Curriculum & Content Management**: Publish course lesson modules, interactive resources, and study material uploads.
- **Quiz Creator & Manager**: Create, edit, and publish custom multiple-choice quizzes with configurable XP rewards and instant broadcast to student devices.
- **Micro-Challenges & Coding Hub**: Track student progress across external coding platforms (LeetCode, Codeforces, GitHub) and clinical/technical challenge sets.
- **Cross-Tab Live Synchronization**: Seamless real-time state syncing between the Faculty CMS and Student Portal using browser `StorageEvent` and localStorage listeners.

### 🔐 3. Authentication & Identity Portal (`login.html`)
- **University School ID Login**: Standard email and password authentication with client-side credential verification.
- **One-Click Student Demo Resume**: Quick-access profile launcher (e.g., "Maya Chen" demo profile) for fast testing and grading demonstrations.
- **Simulated Google OAuth Account Chooser**: Interactive Google Sign-In modal supporting multiple student account personas.
- **Live Google Cloud Identity Services (GIS)**: Integrated official Google Identity Services SDK allowing users to provide their own Google Cloud OAuth Client ID for real Google One-Tap and JWT authentication.
- **Universal Session Sharing**: Unified `localStorage` session state (`xplore_user_session`) shared across all portal pages.

---

## 🏗️ Architecture & File Structure

```
XPlore/
├── index.html        # Student Learning Portal (Dashboard, Quizzes, Streaks, Badges)
├── cms.html          # Faculty CMS & Telemetry Console (Analytics, Quiz Manager, Modules)
├── login.html        # Authentication & Identity Portal (Google GIS, School ID, Session)
├── _redirects        # Clean URL rewrite rules for SPA hosting (e.g., Netlify, Cloudflare)
├── package.json      # Project metadata & local HTTP server scripts
├── .gitignore        # Git ignore rules for node_modules, build archives, and OS files
└── README.md         # Comprehensive project documentation
```

---

## 🌿 Multi-Branch Git Architecture

The repository is organized into dedicated feature branches for collaborative development:

| Branch | Purpose / Scope | Primary Files |
| :--- | :--- | :--- |
| **`main`** | Production-ready unified codebase | `index.html`, `cms.html`, `login.html`, `package.json`, `_redirects` |
| **`index`** | Core student portal & learning dashboard | `index.html`, `package.json`, `_redirects` |
| **`cms`** | Faculty administration, telemetry & quiz management | `cms.html`, `package.json`, `_redirects` |
| **`login`** | Authentication, Google Identity Services & profile state | `login.html`, `package.json`, `_redirects` |

All feature branches (`index`, `cms`, `login`) are tracked and merged into `main` via approved Pull Requests.

---

## 💻 Getting Started Locally

### Prerequisites
- A modern web browser (Google Chrome, Mozilla Firefox, Safari, Microsoft Edge).
- Optional: [Node.js](https://nodejs.org/) (v16+) for running the local development server.

### 1. Clone the Repository
```bash
git clone https://github.com/upadhyaymohit2007777-bit/XPlore.git
cd XPlore
```

### 2. Run the Application

#### Option A: Using NPM (Recommended)
You can launch the included lightweight web server:
```bash
npm start
# or
npm run dev
```
Open your browser and navigate to `http://localhost:3000`.

#### Option B: Using Python HTTP Server
```bash
python3 -m http.server 3000
```
Open your browser and navigate to `http://localhost:3000`.

#### Option C: Direct Browser Opening
Simply double-click or open any of the HTML files directly in your web browser:
- **Student Dashboard**: `index.html`
- **Faculty Console**: `cms.html`
- **Login Portal**: `login.html`

---

## 🌐 Navigation & Route Mapping

When hosted on platforms like Netlify, Cloudflare Pages, or Vercel, the included [`_redirects`](file:///Users/mirai/XPlore/_redirects) file provides clean URLs:

| Route | Target File | Description |
| :--- | :--- | :--- |
| `/` | `index.html` | Student Portal & Dashboard |
| `/cms` | `cms.html` | Faculty CMS & Analytics Console |
| `/login` | `login.html` | Student & Faculty Authentication Portal |

---

## 🛠️ Technology Stack

- **Frontend**: Vanilla HTML5, Modern CSS3 (CSS Variables, Flexbox, CSS Grid, Glassmorphism backdrop filters), Vanilla ES6+ JavaScript.
- **Audio Synthesizer**: Web Audio API (real-time sound effect synthesis without external MP3 dependencies).
- **Authentication**: Official Google Identity Services SDK (`https://accounts.google.com/gsi/client`) + Local Storage Session Provider.
- **Cross-Context Communication**: Browser `StorageEvent` and `localStorage` API for real-time cross-tab updates between faculty authoring and student view.
- **Styling & Fonts**: Google Fonts (`Inter`), customized SVG icons, responsive viewport breakpoints.

---

## 📄 License

This project is open-source software licensed under the [MIT License](LICENSE).
