# CR17 Capital Partners — Landing Page

## Project Goal
A single-page, institutional-grade marketing website for **CR17 Capital Partners**, a growth equity / venture capital direct-investment firm. The site is designed to build trust with Limited Partners (LPs), family offices, and prospective portfolio companies, and to drive inquiries via a clear contact call-to-action.

## Tech Stack
- Static HTML5 + Tailwind CSS (via CDN, configured with a custom navy/gold theme)
- Font Awesome 6 (icons)
- Google Fonts: Inter (body) + Montserrat (headings/display)
- Vanilla JavaScript (mobile nav toggle, scroll-reveal animations, dynamic footer year)
- No backend / database required — this is a purely static, content-driven page

## File Structure
```
index.html                Main single-page site (all sections)
css/style.css              Custom styles: gradients, geometric pattern overlays, card treatments, scroll-reveal
js/main.js                  Mobile menu toggle, IntersectionObserver scroll-reveal, header shadow on scroll, dynamic year
images/cr17-header-logo.png      Official CR17 full logo lockup (gold ribbon mark + "CR17" wordmark + "Capital Partners" tagline) provided by the client — used as the top-left header logo
images/cr17-logo-mark.png       Official CR17 gold ribbon/arrow mark on its navy backing (authentic brand asset provided by the client) — retained in the repo, no longer shown in the header (superseded by the full logo lockup)
images/cr17-brand-logo.jpg       Original full CR17 Capital Partners logo asset (navy card, gold mark + white wordmark) — retained in the repo, no longer displayed in the header (superseded by the text + mark header treatment)
images/cr17-namecard-reference.jpg  Reference image of the CR17 business card (Kevin Zeng) used to inform the site's navy/gold brand palette — not displayed on the page
README.md                   This file
```

## Completed Features
1. **Sticky Navigation Header** — top-left brand lockup using the official full CR17 logo (gold ribbon mark + "CR17" wordmark + "Capital Partners" tagline, authentic asset provided by the client), enlarged to fill nearly the full header height (h-16 / md:h-24, vertical nav padding trimmed to py-1.5 to maximize logo size), anchor links to each section, "Contact Us" button, responsive mobile hamburger menu.
2. **Hero Section** (`#hero`) — bold large-format headline, sub-headline ("A disciplined direct-investment firm backing high-potential companies in robotics, low altitude economy, AI infrastructure, biotech & medical devices and advanced manufacturing."), "Contact Us" CTA button linking to the contact section, and a supporting 5-item stats strip (check size, ownership model, market access, Operational Partnership, regulated entity). The hero text block (headlines + intro paragraph) and the stats strip share the same `max-w-6xl` container width so their left/right edges align.
3. **Investment Strategies** (`#strategies`) — heading rendered as a proper responsive `<h2>` (text-[1.75rem] → 4xl → 5xl) with breathing-room padding above/below (`pb-12 md:pb-20`) so it never crammed-wraps on mobile; then 5 icon-led cards: Early Stage Venture, Growth Equity, Pre-IPO Anchors, Sector Focus (Robotics supply chain, low-altitude economy supply chain, AI / compute hardware supply chain, biotech & medical devices, and advanced manufacturing), Check Size.
4. **LP Value Proposition** (`#lp-value`) — 4 icon-led value points: Direct Ownership/No Layered Fees, Disciplined & Patient Capital, Full Transparency, Proven Family-Office Backing.
5. **Portfolio Company Value Proposition** (`#company-value`) — 4 icon-led value points: Capital + Commercial Partnership, Overseas Market Access, Joint Venture Enablement, Pre-IPO Stability.
6. **Contact / Footer** (`#contact`) — general inquiries email, office phone (clickable `mailto:`/`tel:` links), business registration number, CE number, copyright.
7. **Design system** — dark navy base (`#0a1828` family, incl. `#111f30`/`#060f1c` shades) with a single brand gold accent (`rgb(211, 184, 70)` / `#d3b846`) used for all gold text and icons, abstract geometric gradient overlays (no stock photography), Inter/Montserrat typography pairing, scroll-triggered fade-up reveal animations, fully responsive (mobile, tablet, desktop). Colors were calibrated to exactly match the official CR17 name card brand identity per the client's design brief.
8. **Normalized two-tone text/icon rule (client directive)** — per the client's color directive: **all** white / light-grey / light-blue text across the site is unified to pure white `rgb(255, 255, 255)`, and **all** gold text and icon colors are unified to the name-card gold `rgb(211, 184, 70)` / `#d3b846`. This is implemented by overriding the Tailwind `navy-300/400/500` text tokens to pure white and collapsing the `gold` scale to `#d3b846` in the Tailwind config, plus updating every inline `style="color:…"` override and all gold hex/`rgba()` values in `css/style.css` to match.
8. **Harmonized text coloring** — a single consistent muted-blue-grey tone (`text-navy-300`, `#94a3b8`) is used for all secondary/body copy across every section (nav links, stat labels, card descriptions, contact captions), with white reserved for headings and gold reserved for accents/labels/CTAs — ensuring visual consistency site-wide.
9. **"CR17 always gold" typography rule** — per the brand brief, the "CR17" name is rendered in the primary gold accent color everywhere it appears as a standalone wordmark (both "Why Partner with CR17?" headings, the footer wordmark), while "Capital Partners" / "CapitalPartners" remains white — mirroring the hierarchy on the physical name card.
11. **Light-periwinkle content sections with navy cards (user manual edit)** — per the client's latest in-editor styling pass, the entire **Investment Strategies** (`#strategies`) and **Portfolio Companies** (`#company-value`) sections now use a very light periwinkle/lavender background (`rgb(214, 218, 242)`). On top of this light field, the 5 strategy cards and the 4 Portfolio Companies value rows are solid deep navy (`rgb(40, 51, 124)` / `#28337c`) with white text, and the section headings ("Our Investment Strategies", "Why Companies Partner with CR17?"), the "Capital that opens doors" tagline, and the section body copy are rendered in the same deep navy for a crisp navy-on-light look. The Portfolio Companies container carries `color: rgb(40, 51, 124)` so default text inherits navy.
12. **Flat navy backgrounds on hero / For LPs / Contact (client directive)** — Sections 1 (hero), 3 (For LPs `#lp-value`), and 5 (Contact `#contact`) now use a flat, uniform deep navy `rgb(40, 51, 124)` with **no gradient, vignette, or geometric pattern overlay**. The hero's `hero-bg` gradient class, its gradient overlay div, and the `geo-pattern` / `geo-pattern-2` decorative overlays on all three sections were removed so each section is a single solid navy field with white/gold text on top.
10. **Gold divider lines** — all major section borders (header bottom border, top borders of Strategies / For LPs / For Portfolio Companies / Contact sections, the hero stats-strip divider, the footer's inner divider, and the mobile menu border) use subtle gold-tinted borders (`border-gold/10` / `border-gold/20`) instead of neutral white borders, reinforcing the gold-accent-on-dark brand language from the name card's back design.

## Page Sections / Anchors (single page — no routing needed)
- `/index.html#hero` — Hero banner
- `/index.html#strategies` — Our Investment Strategies
- `/index.html#lp-value` — Why Partner with CR17? (For LPs)
- `/index.html#company-value` — Why Partner with CR17? (For Portfolio Companies)
- `/index.html#contact` — Contact Us / Footer

## Data & Storage
This is a static informational page with no forms, database, or dynamic data source. All contact details (email, phone, CE number, SFC license type) are hard-coded directly into `index.html` and the footer copyright year is set by JavaScript at load:
- Email: Info@CR17CapitalPartners.com
- Phone: +852 2383 7738
- CE #: BCP239
- Hong Kong SFC License: Type 4 (Advising on Securities) & Type 9 (Asset Management)

No RESTful Table API or database tables are used in this project.

## Not Yet Implemented / Potential Next Steps
- A working contact **form** (name/email/message) is not included since form submissions require backend processing; currently "Contact Us" scrolls to a section with direct `mailto:`/`tel:` links. If a form is desired, it could be connected to a third-party form service (e.g., Formspree) which is CORS/no-auth friendly.
- No analytics/tracking script included (can add Google Analytics/GTM snippet if desired).
- No dedicated legal/compliance disclaimer page or cookie consent banner — recommended addition given the regulated financial nature of the firm.
- No multi-language support (currently English only).
- Tailwind is loaded via CDN for rapid development; for a production deployment at scale, consider compiling Tailwind via CLI/PostCSS to reduce payload size and remove the console dev warning.

## Deployment
To publish this site live, use the **Publish tab** in the builder — it will handle hosting and provide a live URL automatically.
