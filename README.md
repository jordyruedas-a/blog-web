## 🚀 Technical Deep Dive & Interactive Features

### 1. Design System & UI/UX (Vanilla CSS)
- **Typography:** Uses `Space Grotesk` for clean, modern headers and `JetBrains Mono` for technical code tags, both imported dynamically from Google Fonts.
- **Layout & Grid:** The entire site is built using **CSS Grid** and **Flexbox** without any external libraries. The "Skills" and "Projects" sections use `grid-template-columns: repeat(auto-fit, minmax(...))` to automatically adapt from a 3-column desktop layout to a single-column mobile layout.
- **Dark Theme Aesthetic:** A deep, gradient-based dark palette (`#080c14` to `#0d1321`) with high-contrast neon accents (`#3b82f6` and `#8b5cf6`) to ensure readability and visual appeal.

### 2. Bilingual Support System (Vanilla JavaScript)
- **Custom Localization Engine:** Instead of using a heavy framework, the site uses a custom JSON translation object (`TRANSLATIONS` object in `app.js`). 
- **Data Attributes:** All translatable text elements are tagged with `data-i18n`, `data-proj`, `data-edu`, `data-exp`, and `data-contact` attributes.
- **Dynamic DOM Replacement:** When the user clicks the `ES/EN` toggle in the sidebar, the JavaScript loops through all tagged elements and updates their `innerHTML` instantly, without reloading the page. This is a highly efficient, lightweight solution for internationalization.

### 3. Interactive JavaScript Components
- **Typed.js Simulation:** The hero section features a custom, vanilla-JavaScript typing effect. It iterates through a list of roles (e.g., "Data Analyst", "Software Engineer"), typing them out character by character, pausing, and then deleting them in a continuous loop.
- **Intersection Observer Animations:** The "Reveal" effects (where cards and progress bars slide up and fill as you scroll) are powered by the native `IntersectionObserver` API. This ensures high performance by only triggering animations when the specific section enters the viewport.
- **Project Filtering System:** The "Projects" section includes an interactive filter bar (Full-Stack, Data Science, IA, Web). This is achieved using vanilla JS event listeners that filter the `data-cat` attribute of the project cards, hiding and showing elements without a page reload.

### 4. Accessibility & Responsiveness
- **Semantic HTML:** Uses `<nav>`, `<main>`, `<section>`, and `<footer>` tags to ensure screen readers can navigate the content logically.
- **Responsive Sidebar:** The fixed left sidebar transforms into a mobile-friendly bottom navigation bar on screens smaller than 900px using CSS media queries (`@media (max-width: 900px)`).
- **Back-to-Top Button:** A floating action button appears dynamically after the user scrolls down 400 pixels, allowing for quick navigation back to the hero section.

---

## 🧪 How to Run & Deploy

Because this is a single HTML file, it does not require a complex backend to run. 


