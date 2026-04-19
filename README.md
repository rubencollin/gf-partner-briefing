# GritFuel — Partner Briefing

A static microsite for the April 2026 partner recalibration. Walks Tlali, Micha, and Kim through the solo sprint output and the decisions that need the four of us before the 29 April 2026 go-live.

## Structure

```
partner-briefing/
├── index.html              Overview + how-to-use + 5 theme cards
├── 01-strategy.html        BMC, JTBD/VPC, Founder persona, Market Size, PMF
├── 02-product.html         GritFuel OS: 5 tools + Monthly Playbook
├── 03-brand.html           Brand Guide v2 (builds on 2025 guide)
├── 04-finance.html         Fixed-cost model, capacity, Scoping, ALC, pricing
├── 05-gtm.html             Assumption-to-tactic map, PMF, onboarding flow
├── assets/
│   ├── styles.css          Shared stylesheet (~280 lines)
│   ├── brand-assets/       Logo + arrow PNGs (charcoal + white variants)
│   └── playbook-preview.jpg
├── artefacts/              Live HTML tools + canvases (open in new tab)
├── downloads/              XLSX, DOCX, PDF — partner-side downloads
└── README.md               this file
```

Every section follows the same shape:

1. **Hero** — one-line frame of the shift
2. **Starting point vs current landing** — two-card split: what gritfuel.works says today vs what the sprint produced
3. **Key decisions** — locked (green) and open (orange) calls
4. **Artefacts** — cards linking to the live HTML tools and downloadable docs
5. **Asks** — three specific questions per section
6. **Pager** — prev / next

## Running locally

No build step. Pure static HTML + CSS.

```bash
cd partner-briefing
python3 -m http.server 8000
# open http://localhost:8000
```

Or simply open `index.html` in a browser.

## Publishing to GitHub Pages

1. Push the `partner-briefing/` folder to a repo (or make this folder the repo root).
2. In the repo on github.com, go to **Settings → Pages**.
3. Source: **Deploy from a branch**. Branch: `main` (or whatever you're using). Folder: `/partner-briefing` (or `/` if you made this the root).
4. Save. GitHub Pages will publish to `https://<org>.github.io/<repo>/` within a minute or two.

Custom domain (e.g. `partners.gritfuel.works`): add a CNAME record pointing at `<org>.github.io`, then enter the domain in **Settings → Pages → Custom domain** and enable **Enforce HTTPS**.

## What partners should do

1. **First pass — skim all five overviews** (~25 min). Just the narrative and decision blocks. Don't open artefacts yet.
2. **Second pass — open artefacts in your lane.** Tlali: Strategy + GTM. Micha: Product + Finance. Kim: Brand + GTM. Click through the live tools.
3. **Reply with reactions, not edits.** Each section ends with three specific questions — hit those first. Free-form thoughts welcome after.
4. **Working session** — 23–25 April. We close any outstanding calls then run the refinement pass before 29 April go-live.

## Timeline

| Date              | What                                            |
|-------------------|-------------------------------------------------|
| 18–22 April 2026  | Partner review window (async)                   |
| 23–25 April 2026  | Working session + refinement pass               |
| 29 April 2026     | gritfuel.works go-live with recalibrated story  |

## Version

v1.0 — 18 April 2026 — prepared by Ruben.

After go-live, this briefing becomes a living library we update as we learn from cohort one.
