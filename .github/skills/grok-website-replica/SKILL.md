---
name: grok-website-replica
description: "Create a detailed, copy-ready Grok AI prompt to rebuild this Shan portfolio website as closely as possible. Use when asking Grok to clone, recreate, or build the same website from its live URL, screenshots, or project files."
argument-hint: "Optional: add a target framework, special requirements, or reference screenshots"
user-invocable: true
---

# Grok Website Replica Brief

Create a complete, evidence-based build brief that the user can paste into Grok AI to recreate the Shan portfolio website in this project. Focus on visual fidelity, responsive behavior, content, and working interactions—not a loose redesign.

## Reference website

- Live reference: <https://shan-portfolioo.netlify.app>
- Repository reference (if Grok can access GitHub): <https://github.com/shajith23/shan-portfolio>
- Local entry page: `index.html`
- Local assets and original implementation: `assets/`

The local project is the strongest source for exact copy, image selection, page structure, and interaction details. The live site is the strongest source for the rendered visual result. If the user has not supplied files to Grok, clearly tell them to attach the repository ZIP (including `assets/`) and screenshots; do not imply Grok can read their local disk paths.

## Procedure

1. Inspect the supplied website URL, screenshots, and project files when available. Treat the existing homepage as the source of truth. If a source is unavailable, say so in the Grok prompt and ask Grok not to invent unseen details.
2. Describe the page from top to bottom, using the homepage blueprint below. Verify labels and content against `index.html` when project files are accessible; don't present the README's broad feature list as proof that every item appears on the homepage.
3. Explain the visual system from observed evidence: page backgrounds, typography, scale and weight, color palette, spacing, content widths, image crops, borders, and hover/focus states. Do not guess exact colors, fonts, or measurements when they cannot be inspected; instruct Grok to derive them from the supplied reference.
4. Include responsive requirements for desktop, tablet, and mobile. Ask Grok to inspect the reference at multiple viewport sizes if browser access is available, and to preserve the actual mobile navigation and section order rather than simply shrinking the desktop layout.
5. Describe the existing interactions: preloader, sticky header, responsive/off-canvas navigation, hover treatments, scroll-triggered reveals, marquee, sliders, counters, and back-to-top control as applicable. Require keyboard support, reduced-motion handling, and working destinations for links and buttons.
6. Produce one self-contained, clearly titled prompt the user can copy directly into Grok. Include the reference URLs, required materials, detailed specification, implementation constraints, and a verification checklist. Use plain language, not unexplained class names.
7. Ask Grok to implement the website, not just explain how to build it. Require it to inspect the supplied project before editing, retain reusable assets, avoid unnecessary dependencies, and report any inaccessible references or missing assets explicitly.

## Homepage blueprint

Use this as a verified starting outline, then add exact details from the source files and visual reference:

1. **Header/navigation:** Portfolio identity/logo, desktop navigation and a prominent CV-download action; provide the appropriate responsive menu on smaller screens.
2. **Hero:** Large, bold “developer” headline; centered portrait/figure artwork; introduction (“Hello! I'm Shan” and digital designer/creative developer role); a list of five offerings (Web Development, Branding & Identity, Creative Strategy, UI/UX Design, Digital Marketing); central design/branding/web-development statement and project CTA; compact experience/stat counters on the right.
3. **About:** Large centered statement, image beside biography copy, and a circular about action/counter treatment.
4. **Services transition and services:** Repeating “Services” marquee, followed by a dark service panel with numbered service rows, titles, and skill/category tags. Preserve every row and its order from the supplied source.
5. **Portfolio/work:** Work/projects area with large project imagery, titles, categories, and linked project actions. Preserve the original order, image choices, and asymmetrical layout.
6. **Testimonials:** Introductory statement and testimonial cards/slider with client identity and role where shown.
7. **Client/brand strip:** “Loved by Teams Around the World” heading and the original brand/logo items.
8. **Contact/footer:** “Let’s create something meaningful” contact invitation, email and phone links, contact form and social links where present, footer navigation, and return-to-top action.

Keep the observed section order and approximate visual hierarchy. The list above is a structural guide, not permission to fabricate missing portfolio entries, testimonial text, logos, or contact details.

## Verified implementation clues

When the project files are supplied, use these to help Grok preserve the original:

- The homepage is a static HTML page using Bootstrap 5, custom CSS, and JavaScript. Existing files are under `assets/css/` and `assets/js/`; do not migrate frameworks unless the user explicitly asks.
- Images, logos, icons, and shapes live under `assets/images/`. Reuse the matching local assets rather than substituting generic stock imagery.
- The current page uses GSAP (including ScrollSmoother/ScrollTrigger), AOS, Swiper, jQuery, Magnific Popup, and PureCounter. Preserve or deliberately reproduce their visible behaviors; avoid adding duplicate libraries.
- Existing content and sections are in `index.html`. Existing interaction setup is in `assets/js/main.js` and `assets/js/slider-active.js`; confirm actual usage before changing behavior.
- The original implementation includes a loading transition, a header that becomes fixed after scrolling, mobile/off-canvas navigation, scroll reveals, a magic cursor, marquee content, sliders, and a back-to-top button. Reproduce the reference behavior where visible and ensure graceful behavior when motion is reduced or scripts fail.
- The public page metadata calls the site “Shan - Digital Agency & Creative Portfolio”; its visible identity is Shan's personal portfolio. Do not replace its brand identity with a generic agency template.

## Required shape of the Grok prompt

The copy-ready prompt should contain these sections:

1. **Role and objective** — tell Grok to build a close visual and functional recreation of the supplied website, not a redesign.
2. **Reference material** — list the live URL and identify the attached project ZIP/screenshots. Explain that local paths are not accessible unless files are uploaded.
3. **Visual inspection instructions** — inspect full-page and viewport screenshots; note exact observed geometry, typography, colors, image placement/crops, and responsive differences; identify anything that cannot be verified.
4. **Page-by-page/section specification** — describe the header, every homepage section, content hierarchy, imagery, and footer in source order.
5. **Design and responsive rules** — match the reference's visual language and behavior across desktop, tablet, and mobile; prevent overflow and preserve legibility and touch targets.
6. **Interactions and accessibility** — specify menus, links, forms, sliders, hover/focus states, scroll effects, reduced motion, semantic HTML, keyboard operation, and accessible names.
7. **Implementation requirements** — inspect supplied files first; preserve appropriate assets/content; use the existing stack unless instructed otherwise; keep links and forms functional; report missing information instead of fabricating it.
8. **Acceptance checklist** — compare screenshots at desktop (1440px), tablet (768px), and mobile (390px) or the closest available sizes; check every section, text, image, navigation action, console/network errors, and horizontal overflow; iterate on visible mismatches.

The prompt must be standalone and ready to paste, with no references such as “follow the instructions above.” If the user requests only the Grok prompt, do not modify the website code. If the user instead asks to implement the replica in this workspace, follow the normal project workflow and make the changes here.
