# Parallax Effect — Adventure Scrolling Webpage

> A smooth, CSS-only parallax scrolling experience built for adventure enthusiasts, no JavaScript, no libraries, just pure HTML & CSS magic.

---

## Table of Contents

- [Overview](#overview)
- [Tools and Technologies](#tools-and-technologies)
- [Project Structure](#project-structure)
- [Methods](#methods)
- [Key Insights](#key-insights)
- [Output](#output)
- [How to Run This Project](#how-to-run-this-project)
- [Result and Conclusion](#result-and-conclusion)
- [Future Work](#future-work)
- [Author and Contact](#author-and-contact)

---

## Overview

This project demonstrates the **CSS Parallax Scrolling technique**, a visual effect where background layers move at different speeds relative to the foreground as the user scrolls, creating a stunning illusion of depth and motion.

The theme is **Adventure** - featuring three activity panels (Biking, Rafting, Surfing) with fixed-attachment background images that create the classic parallax feel. The entire effect is achieved using CSS `perspective`, `transform: translateZ()`, and `background-attachment: fixed` : **zero JavaScript required**.

This project is ideal for showcasing:
- Deep understanding of the CSS 3D rendering pipeline
- Mastery of `transform-style: preserve-3d` and `perspective` stacking
- Clean, semantic HTML structure
- Responsive design considerations

---

## Tools and Technologies

| Technology | Purpose |
|---|---|
| **HTML5** | Semantic page structure |
| **CSS3** | Parallax effect, layout, typography, 3D transforms |
| `perspective` + `translateZ` | CSS 3D parallax engine for the hero section |
| `background-attachment: fixed` | Parallax effect for inner content panels |
| `transform-style: preserve-3d` | Maintains 3D context across child elements |
| **VS Code** | Development environment |
| **Live Server** | Local dev server for hot reload |

> No JavaScript. No frameworks. No dependencies.

---

## Project Structure

```
Parallax/
│
├── index.html              # Main HTML file — page structure & content
├── Style.css               # All styles — parallax engine + layout + theming
├── dependencies.txt        # Runtime & dev tool requirements
├── README.md               # Project documentation (this file)
│
└── Assets/                 # Image assets used in parallax panels
    ├── 360_F_...jpg        # Hero background — mountain/sky scene
    ├── Untitled design.png # Hero foreground — layered adventure graphic
    ├── images.jpeg         # Biking panel background
    ├── istockphoto-...jpg  # Rafting panel background
    └── 1-tipi_tsh05431.jpg # Surfing panel background
```

---

## Methods

### 1. CSS 3D Parallax (Hero Section)
The hero uses the browser's native 3D rendering engine

### 2. Fixed Background Parallax (Content Panels)
The three activity sections use a simpler, widely-supported technique

---

## Key Insights

- **Two parallax techniques** are combined: CSS 3D transforms (hero) and `background-attachment: fixed` (panels) - each optimal for its use case.
- The `perspective` property **must be on the scroll container** (`.wrapper`), not the body, so the effect tracks with scroll position correctly.
- `scale()` is a required companion to `translateZ()` to avoid elements appearing zoomed out.
- `background-attachment: fixed` does **not work on iOS Safari**, a known browser limitation for mobile. A JS-based fallback (e.g. Intersection Observer) would be needed for full mobile support.
- **No JavaScript** means instant load, zero layout shift, and perfect Lighthouse performance scores.

---

## Output

The page renders three distinct visual zones:

| Section | Effect | Description |
|---|---|---|
| **Hero** | CSS 3D Parallax | Background drifts at 1/5th the scroll speed; foreground at ~2/3 speed |
| **Biking Panel** | Fixed Background | Mountain biking imagery with centred label badge |
| **Rafting Panel** | Fixed Background | River rafting scene with centred label badge |
| **Surfing Panel** | Fixed Background | Ocean surfing imagery with centred label badge |

**Live Preview:** Open `index.html` directly in any modern browser - no build step needed.

---

<a name="how-to-run-this-project"></a>

## How to Run This Project

### Option 1 — Open directly (simplest)
```bash
# Clone the repository
git clone https://github.com/ManasGulati/Parallax.git

# Open in browser
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### Option 2 — VS Code Live Server (recommended for development)
1. Install [VS Code](https://code.visualstudio.com/)
2. Install the **Live Server** extension by Ritwick Dey
3. Right-click `index.html` -> **"Open with Live Server"**
4. Browser auto-opens at `http://127.0.0.1:5500`

> No npm install. No build commands. No configuration.

---

<a name="result-and-conclusion"></a>

## Result and Conclusion

The project successfully demonstrates a **silky-smooth parallax scrolling experience** using only native browser CSS capabilities. The dual-technique approach (3D transforms for the hero & fixed background for panels) shows an understanding of when to use each method based on performance and compatibility trade-offs.

Key achievements:
- Zero JavaScript, lightweight and instantly loadable
- Smooth 60fps scrolling performance on desktop browsers
- Clean, well-commented CSS architecture
- Modular structure making it easy to swap themes or images

---

## Future Work

- [ ] **Mobile support** : Add an Intersection Observer JS fallback for `background-attachment: fixed` on iOS Safari
- [ ] **Smooth scroll snapping** : Add CSS `scroll-snap` for section-by-section navigation
- [ ] **Dynamic content** : Replace placeholder Lorem Ipsum with real adventure travel copy
- [ ] **Accessibility** : Add `prefers-reduced-motion` media query to disable parallax for users who prefer minimal motion
- [ ] **Dark/Light toggle** : CSS custom properties (`--var`) based theme switcher
- [ ] **Navigation bar** : Fixed header with smooth anchor links to each section
- [ ] **Animations** : Fade-in text using `@keyframes` + Intersection Observer on scroll

---

## Author and Contact

**Manas Gulati**
Frontend Developer

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ManasGulati)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/manasgulatiryu)

📧 [manasgulati222@gmail.com](mailto:manasgulati222@gmail.com)

> 📬 Feel free to open an issue or reach out if you'd like to collaborate or give feedback!

---

<p align="center">Made with ❤️ and pure CSS</p>
