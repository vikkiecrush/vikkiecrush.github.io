# Victory Ikpe — Professional Portfolio

Personal portfolio site for **Victory Ikpe**, Senior Data Scientist and Emerging AI/ML Leader.

**Live at:** [https://vikkiecrush.github.io](https://vikkiecrush.github.io) *(after deployment — see DEPLOY.md)*

---

## What's inside

- `index.html` — Landing page: hero, bio, personal value proposition, artifacts grid, personal, contact.
- `artifacts/nil-pick-detective.html` — Artifact 1: Custom GPT for grocery-fulfillment root-cause analysis.
- `artifacts/aiml-evolution.html` — Artifact 2: Research timeline of AI's evolution 1943 – present.
- `assets/styles.css` — Custom styling on top of Tailwind CDN.
- `assets/images/` — For any images added later (profile photo, artifact screenshots).
- `assets/docs/` — For downloadable PDFs or supporting docs.
- `.nojekyll` — Tells GitHub Pages to skip Jekyll processing (we're serving plain HTML).

## Tech stack

- **HTML5** — semantic, accessible markup.
- **Tailwind CSS (CDN)** — utility-first styling, no build step.
- **Google Fonts** — Fraunces (display serif) + Inter (body sans).
- **Vanilla JavaScript** — smooth scrolling only, no frameworks.
- **GitHub Pages** — free static hosting.

## Design principles

- **Mobile-first responsive** — works on phones, tablets, desktops.
- **WCAG 2.2 AA** — focus states, color contrast, semantic headings, reduced-motion support.
- **Zero build step** — Tailwind via CDN keeps this portable and simple (Zen of Python).
- **Palette:** slate-950 base, brand emerald `#10b981`, brand amber `#f59e0b`, brand deep-emerald `#064e3b`.

## Adding a new artifact

1. Copy `artifacts/nil-pick-detective.html` to `artifacts/your-new-artifact.html`.
2. Update all 10 required sections (Title, Introduction, Description, Objective, Process, Tools, Value Proposition, Unique Value, Relevance, References).
3. In `index.html`, replace one of the "Artifact 3/4/5 · Coming Soon" placeholder cards with a real card linking to your new page.
4. `git commit` and `git push` — GitHub Pages will redeploy automatically.

## Deployment

See [DEPLOY.md](DEPLOY.md) for step-by-step GitHub Pages setup.

---

*Built as part of AIML-500 at Indiana Wesleyan University. Portfolio structure and styling were drafted with AI coding assistance; all career decisions, artifacts, and analytical conclusions are Victory's own work.*
