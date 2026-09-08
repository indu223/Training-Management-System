# Training Management System

A fully interactive, client-side Training Management System built as a single-page application.  
Live demo: **https://indu223.github.io/Training-Management-System/**

---

## Features

| Module | Capabilities |
|---|---|
| **Dashboard** | Live stats: Courses, Trainers, Learners, Upcoming Sessions, Certificates Issued |
| **Courses** | Full CRUD · Search · Filter by Mode/Status · Sort · CSV Export · CSV Import |
| **Trainers** | Full CRUD · Search · Filter by Status · CSV Export |
| **Learners** | Full CRUD · Search · Filter by Department/Status · Progress tracking · CSV Export |
| **Schedule** | Full CRUD · Search · Filter by Mode/Status · CSV Export |
| **Global Search** | Cross-module instant search from the top bar |

## Technology Stack

- **HTML5 / CSS3** — single `index.html` entry point
- **Bootstrap 5.3** — responsive layout, modals, badges (CDN)
- **Bootstrap Icons 1.11** — icon set (CDN)
- **Vanilla JavaScript (ES6+)** — no frameworks, no build step
- **LocalStorage** — all data persists in the browser; no backend required

## Project Structure

```
Training-Management-System/
├── index.html      ← entire application (HTML + CSS + JS)
├── .gitignore
└── README.md
```

Everything is self-contained in `index.html`.  
All external dependencies are loaded from CDNs — no npm, no Node.js, no server.

---

## Enabling GitHub Pages

1. Push this repository to GitHub (see below).
2. Go to **Settings → Pages** in your GitHub repository.
3. Under **Source**, select **Deploy from a branch**.
4. Choose branch: `main` (or `master`), folder: `/ (root)`.
5. Click **Save**.
6. GitHub will publish the site at:  
   `https://<your-username>.github.io/<repository-name>/`

> GitHub Pages may take 1–2 minutes to go live after the first push.

---

## Deploying / Updating

```bash
# First time
git clone https://github.com/indu223/Training-Management-System.git
cd Training-Management-System

# Make changes to index.html, then:
git add .
git commit -m "Your change description"
git push origin main
```

GitHub Pages re-deploys automatically on every push to the configured branch.

---

## Sample Data

On first load the app seeds the following sample records:

**Courses** — Excel for Beginners · Advanced Excel · Power BI Fundamentals · Python Basics · AI with IBM watsonx · Project Management Essentials · Communication Skills · Leadership Foundations

**Trainers** — John Smith · Sarah Lee · Mark Johnson · Emily Chen · David Tan

**Learners** — 10 sample learners across Finance, IT, HR, Operations, and Sales

**Sessions** — 5 scheduled sessions linked to the above courses and trainers

All data is stored in `localStorage` under the keys `tms_courses`, `tms_trainers`, `tms_learners`, `tms_sessions`.

---

## Resetting Data

To reset all data to seed defaults, open the browser DevTools console and run:

```js
['tms_courses','tms_trainers','tms_learners','tms_sessions'].forEach(k => localStorage.removeItem(k));
location.reload();
```

---

## License

© SmartStack
Designed & Developed by **SmartStack**


