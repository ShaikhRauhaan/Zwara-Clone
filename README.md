1.) Download or clone the repo.
2.) Open index.html in your browser (or run a local server):
3.) Edit index.html and css/styles.css to customize content and styles.

Short step-by-step to recreate (mobile-first)
1.) Plan sections — map the page: header/nav, hero, features/menu/listings, CTA, footer.
2.) Create semantic HTML — use <header>, <nav>, <main>, <section>, <article>, <footer>. Keep content structure clear.
3.) Base (mobile) styles — set base font-size, line-height, and a single-column layout. Make images max-width:100%; height:auto;.
4.) Grid for major layout — use CSS Grid to create multi-column areas on larger screens:
.page {
  display: grid;
  gap: 1.5rem;
  grid-template-columns: 1fr;
}
@media (min-width: 768px) {
  .page { grid-template-columns: repeat(12, 1fr); }
  .hero { grid-column: 1 / 9; }
  .aside { grid-column: 9 / 13; }
}

5.) Flex for components — use Flexbox for nav, card groups, and horizontal alignment:
.nav { display: flex; align-items: center; justify-content: space-between; }
.cards { display: flex; gap: 1rem; flex-wrap: wrap; }

6.) Responsive breakpoints — add media queries at ~480px, 768px, and 1200–1440px to adjust grid columns, font sizes, and spacing.
7.) Navigation & hamburger — for small widths hide the full menu and show a hamburger (CSS-only or minimal JS to toggle .open class).
8.) Images & assets — use <picture> or optimized srcset for responsive images; compress files for performance.
9.) Accessibility — add alt, ensure focus styles, & make interactive elements keyboard-accessible.
10.) Test — check on mobile, tablet, desktop and different browsers.

11.) Project Structure
/zwara-clone
  ├─ index.html
  ├─ README.md
  ├─ css/
  │   └─ styles.css
  ├─ js/
  │   └─ main.js     # optional (hamburger toggle)
  ├─ images/
  └─ assets/
  
12.) Tips & best practices:-
Use rem units for scalable typography.
Prefer max-width containers (e.g., max-width: 1200px; margin: 0 auto;) for large screens.
Keep CSS modular: layout rules (grid), components (cards/nav), utilities (spacing).
Lazy-load large images where possible (loading="lazy").
Run Lighthouse to check performance & accessibility.

