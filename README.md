# Developer and Researcher Portfolio Website

> Official developer, researcher, and academic portfolio of Nhut Nguyen (@nhdnhut).
> Standalone Zero-Dependency Architecture | Semantic HTML5 | Responsive CSS3 | Vanilla JavaScript | Markdown-Driven Articles | GitHub Pages Ready

[![GitHub Pages](https://img.shields.io/badge/Deployment-GitHub_Pages-222222?style=flat-square&logo=github&logoColor=white)](https://nhdnhut.github.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

---

## 1. Overview

This repository hosts the official personal website and academic archive of Nhut Nguyen (@nhdnhut), an Artificial Intelligence student and systems researcher at the University of Information Technology (UIT, VNU-HCM).

The site is built with a dependency-free, static-first architecture that runs out of the box on GitHub Pages without requiring a node build step, npm packages, or server runtimes.

Key Sections:
- About: Academic background, research philosophy, and technical skills.
- Works and Research: Empirical benchmarks, neural network optimizations, and publications.
- Projects: Interactive applications, developer tools, and systems software.
- Field Notes / Writing: Bilingual (English / Vietnamese) Markdown-rendered research notes and field essays.
- Reading Archive: Curated library of foundational textbooks, notes, and technical literature.
- Timeline: Verified academic and project milestones.

---

## 2. Architecture and Data Flow

All visible content, navigation links, and theme parameters are centrally governed by `config/portfolio.config.js`:

```text
developer-portfolio/
├── config/
│   ├── portfolio.config.js        # Central content, projects, and metadata configuration
│   └── generated/
│       └── writing-content.js     # Bundled fallback for offline file-protocol browsing
├── css/
│   └── styles.css                 # Typography, themes (light/dark), and responsive grid
├── js/
│   ├── site.js                    # Header, footer, theme toggler, and routing
│   └── writings.js                # Dynamic Markdown fetcher and renderer
├── writings/                      # Bilingual Markdown articles (.en.md and .vi.md)
├── assets/                        # Profile imagery, icons, and document PDFs
├── vendor/                        # Lightweight local Markdown parser
├── index.html                     # Home / Biography
├── research.html                  # Research papers and academic projects
├── projects.html                  # Software systems and open-source tooling
├── books.html                     # Academic reading list
├── blog.html                      # Field notes archive
├── writing.html                   # Dynamic single-article viewer
├── activities.html                # Milestones timeline
├── library.html                   # Resource library
├── LICENSE                        # MIT License
└── README.md                      # Repository documentation
```

---

## 3. Quick Start Guide

### Local Preview
Serve the static files using Python's built-in HTTP server:

```bash
python -m http.server 8080
```

Navigate to `http://localhost:8080` in your web browser.

### Direct File Protocol
The repository includes an offline fallback bundle (`config/generated/writing-content.js`). You can double-click `index.html` to open and navigate the site locally without a running HTTP daemon.

---

## 4. Deployment to GitHub Pages

1. Create a repository named `nhdnhut.github.io` on GitHub under account `@nhdnhut`.
2. Push this repository to the `main` branch:
   ```bash
   git push -u origin main
   ```
3. In repository Settings -> Pages, ensure the source is set to "Deploy from a branch" (branch: `main`, folder: `/ (root)`).
4. The site will be automatically published at `https://nhdnhut.github.io`.

---

## 5. Author and License

- Author: Nguyen Huynh Dang Nhut (@nhdnhut)
- Affiliation: University of Information Technology, VNU-HCM
- License: MIT License (see [LICENSE](LICENSE))

