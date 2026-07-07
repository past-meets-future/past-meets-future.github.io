# Past Meets Future 2026 — Website Plan

Companion to `DESIGN.md` (design language) and `CLAUDE.md` (working conventions). Research verified 2026-07-07 against hcomp.acm.org/2026, ci.acm.org/2026, and the prior workshop sites.

---

## 1. Verified Facts (single source of truth for site copy)

**Official 2026 title (per conference listings — use everywhere, including `<title>` and OG card):**
> Past Meets Future: 3rd Annual Workshop on Human-AI Interaction for **Digital Humanities** and Cultural Heritage

Note: the series' earlier editions said "Digital History." The accepted 2026 proposal says "Digital Humanities" — reconcile once, sitewide. (Verify against the accepted proposal PDF before launch.)

- **When:** Sunday, September 27, 2026 (full-day) — the joint HCOMP/CI Workshops Day. (CrowdCamp runs the same day, but this is background only — all CrowdCamp/coordination copy was removed from the site 2026-07-08; make no scheduling-coordination claims.)
- **Where:** Virginia Tech Academic Building One (AB1), 3625 Potomac Ave., Alexandria, VA 22305 — "near Washington, DC." ~5-min walk from Potomac Yard–VT Metro (Blue/Yellow), one stop from DCA. Parking: ParkMobile Zone #85129, $4/hr (≤4h) or $20/day.
- **Host venues (one physical event, jointly badged):** ACM HCOMP 2026 — now officially "The 2026 ACM Conference on Human-AI Complementarity and Alignment" (moved from AAAI to ACM; do NOT call it "Human Computation and Crowdsourcing") — co-located and tightly integrated with the 14th ACM Collective Intelligence Conference (CI 2026), Sept 27–30. **A single registration covers both conferences.** Shared theme: **"Connections"** — echo it in site copy.
- **Workshop status:** already listed as an accepted FULL-DAY workshop on both conference sites (hcomp.acm.org/2026/attend.html#past-meets-future and ci.acm.org/2026/accepted_workshops.html#digital-humanities), both linking to the Google Sites URL we are replacing.
- **2026 organizers (order per conference listing):** Fei Shan (Virginia Tech) · David A. Shamma (Northeastern University Oakland) · Victoria Van Hyning (University of Maryland) · Benjamin Charles Germain Lee (University of Washington) · Vikram Mohanty (Carnegie Mellon University) · Kurt Luther (Virginia Tech).
  Context: Luther is also CI 2026 General Chair; Mohanty is CI 2026 Workshops Co-Chair (both roles are public; describe the review process factually).
- **Timeline (all 11:59pm AoE):**
  - Workshop websites live + CFP announced: June 29, 2026 *(already passed — urgency)*
  - Workshop paper deadline: **July 30, 2026** (confirmed by organizers 2026-07-07; email submission)
  - Acceptance notifications: August 7, 2026
  - Conference early-bird registration: **no date on our site** — the approved copy is "Early-bird registration and its deadline will be announced on the ACM HCOMP 2026 and CI 2026 websites" (organizer decision 2026-07-08; the earlier Aug 22 claim was retracted)
  - Workshop day: September 27, 2026
- **2026 theme:** "From challenges to solutions" — the 2025 edition mapped the field's challenges (Miro board; five clusters: AI–GLAM alignment · cognitive/educational/social impact · incentives · IP/copyright/authorship · ethics); 2026 solicits solutions: systems, prototypes, open source, AR/VR/XR, write-ups, decks. CFP has FOUR formats (position paper / published paper / systems & prototypes / new modalities). **Site copy shows three challenge cards** — incentives and IP/copyright/authorship were dropped from the CFP page (organizer decision 2026-07-08) — plus the full-width "bridge is the method" card, and must always say topics are NOT limited to the map ("The map is not a checklist").
- **Contact:** pastmeetsfuturehaiworkshop@gmail.com · Workshop chairs list: hcomp-ci-2026-workshops@acm.org
- **Past editions:** № 1 — ACM IUI 2024, Greenville, SC (the 2026 Google Sites draft says "Clemson, SC" — the 2024 site and workshop paper say Greenville; verify and use one). № 2 — ASIS&T 2025, near Washington, DC.
- **CFP inheritance (from 2024/2025, to adapt):** three submission formats — (a) new 2–4 page position paper, (b) previously published paper, (c) link to a digital project / video demo; organizers as program committee, single-blind review; at least one author registers and attends.

## 2. Architecture & Hosting

**Pattern:** single repo → GitHub org `pastmeetsfuture`, repo `pastmeetsfuture.github.io`, GitHub Pages deploy-from-branch with `.nojekyll`, **plain hand-written semantic HTML/CSS/JS — no build step.**

Rationale (from comparative research: HAI-GEN, SUMAC, Wikidata Workshop, Wiki Workshop, CHR patterns): stable cumulative URLs (`/2026/`), past years frozen by never editing their folders, zero toolchain to rot between annual bursts, no CI failure that silently blocks a deadline-night fix, and plain HTML's classic costs (boilerplate consistency, hand-rendered tables) are exactly what Claude Code eliminates — while SSG costs (build failures, dependency rot) are infrastructure problems AI cannot fix. Escape hatch: the year-folder structure ports cleanly to Jekyll/Eleventy later without URL changes.

```
pastmeetsfuture.github.io/
├── .nojekyll
├── index.html            ← series landing: current edition + accession ledger
├── 2024/index.html       ← thin archive page (summary + link to original Google Site)
├── 2025/index.html       ← thin archive page (summary + link to ASIS&T page)
├── 2026/
│   ├── index.html        ← hero, dual-venue band, overview, now-showing strip
│   ├── cfp/index.html    ← machine-readable card + essay CFP (print stylesheet)
│   ├── dates/            ← or anchor sections on index — decide during build
│   ├── papers/index.html ← accepted papers (empty-state stamped until Aug 7)
│   ├── people/index.html ← organizers now; speakers/panelists when announced
│   ├── schedule/index.html
│   ├── venue/index.html  ← AB1, Metro, parking, registration facts, access FAQ
│   ├── colophon/index.html
│   ├── data/             ← YAML source of truth: dates.yml, papers.yml,
│   │                        people.yml, schedule.yml (Claude renders → HTML)
│   ├── assets/           ← fonts (subset woff2), css, js, img/ (incl. paper PDFs)
│   └── pmf2026.ics
└── shared/               ← only truly cross-year assets (favicon, ⊕ mark svg)
```

- **PDFs live in the repo** — never personal Drive links (2024's fragility).
- **Custom domain:** optional, deferrable with zero breakage (github.io URLs redirect once added). If bought: `pastmeetsfuture.org`, ~$11/yr (Porkbun/Cloudflare), registered to a shared committee account. Not a launch blocker.
- **Data-file workflow:** YAML files are canonical; organizers edit YAML in the GitHub web UI (or email content to a maintainer); Claude Code regenerates the HTML sections — deterministic, reviewable diffs.

## 3. Build Phases (CFP clock is already running)

**STATUS 2026-07-08: Phase 0 SHIPPED.** Live at <https://past-meets-future.github.io/> (repo: github.com/past-meets-future/past-meets-future.github.io, GitHub Pages from main). Single-page 2026 edition + subpages (cfp/, attend/, colophon/) + archive pages + brand suite in /shared/brand/. Operational docs (README/CLAUDE/DESIGN/PLAN/MAINTENANCE) and agent skills (.agents/, .claude/, skills-lock.json) are tracked so any teammate can clone and work with Claude Code; only vision.md, research/, and the proposal PDF stay local (gitignored — candid deliberations). Note the repo is public: anything committed is world-readable. Remaining launch ops: (1) email hcomp-ci-2026-workshops@acm.org to repoint both conference listings; (2) banner-link the old Google Sites page to the new URL; (3) generate hero textures + og.jpg (prompts in DESIGN.md); (4) Miro board owner-side: set share link to view-only, check sticky-author anonymity (or export frames to PDF into the repo).

**Phase 0 — original checklist:**
1. Repo scaffold, tokens/typography system, ⊕ mark, favicon, OG card.
2. `/2026/` home: Plate I hero, dual-venue band, overview (drop cap), now-showing strip.
3. CFP page (machine-readable card + essay + print stylesheet) — **needs the chosen paper deadline from organizers.**
4. Key-dates ledger + `.ics`.
5. Organizers section (6 cards, duotoned headshots, real alt text).
6. Venue page + colophon. Empty-state cards for papers/speakers/schedule.
7. Root landing + thin 2024/2025 archive pages + accession ledger.
8. Accessibility pass (AA on tinted grounds, both themes) + Lighthouse + 320px/400% zoom check.
9. Launch on GitHub Pages → **email hcomp-ci-2026-workshops@acm.org to repoint both conference listings** (currently → Google Sites). Discovery beats design: this is the highest-priority action item, and the Google Sites page should banner-link to the new site.

**Phase 1 — Aug 7:** accepted papers land (YAML → index cards, similarity edges), notifications copy, schedule flips from "tentative" to final. (Early-registration copy stays "announced on the HCOMP & CI sites" until those sites publish a date.)

**Phase 2 — Aug–Sep:** speakers/panelists plates, full schedule timetable, optional About-page scrubber showpiece, optional Remotion teaser video for social promotion.

**Phase 3 — post-event:** outcomes/photos/proceedings, freeze `/2026/`, append ledger row `ENTRY PENDING · 2027`, write ARCHIVING.md checklist for the 2027 team.

## 4. Asset Pipeline — the Collection (round 2)

The identity's assets are REAL open-access artifacts, not generated art. Pipeline (document as a one-command script in the repo): fetch from source APIs (Met Open Access, AIC IIIF at 843px, LoC IIIF with pct sizing, Smithsonian OA, Rijksmuseum) -> resize to 800/1400w -> AVIF/WebP/JPEG -> `/2026/assets/collection/` + `collection-2026.json` (coords, captions, verbatim rights, task labels). Hotlinking is banned. The 2026 core eight + rotation pool, with verified URLs and rights, live in `research/round2/artifacts.json`. Annotation data is precomputed from real sources (LoC ALTO XML for the Tribune; computed palettes; visible seal/script geometry) — see DESIGN.md §6 for the launch-blocking honesty policy. gpt-image-2 is now OPTIONAL (round 1's ornament plan is retired); if used at all, non-representational assets only, disclosed in the colophon.

## 5. Open Items (need organizer input)

| # | Item | Owner |
|---|---|---|
| 1 | ~~Paper deadline~~ CONFIRMED: July 30, 2026 · email submission | done |
| 2 | ~~Miro URL~~ RECEIVED + linked; owner must set view-only + de-identify | Mohanty |
| 3 | Cross-organizer sign-off on the 2026 collection (8 core + pool); sensitivity review of Wari/Ge'ez framing lines | all six |
| 4 | Named expert reviewers per script before any transcription text ships (Ge'ez, nasta'liq, Nahuatl, classical Chinese) — until then geometry only | Van Hyning lead? |
| 5 | Greenville vs Clemson for IUI 2024 line | anyone |
| 6 | Canonical title wording ("Digital Humanities") vs accepted proposal | Shan/Luther |
| 7 | GitHub org creation + who holds admin (bus-factor: ≥2 organizers) | Mohanty |
| 8 | Repoint conference listings after launch (email workshops chairs — note Mohanty co-chairs) | Mohanty |
| 9 | ~~Headshots~~ RESOLVED: names + affiliations only (organizer decision) | done |
| 10 | Sponsors (Google Sites says TBD) — seal-chip "SUPPORTED BY" row when they exist | organizers |
| 11 | Re-verify museum accession numbers in credit slugs before launch | builder |
| 12 | Keynote speaker confirmation (schedule shows TBA) | organizers |
| 13 | Decide: Miro iframe embed on a /challenges subpage (click-to-load) vs. link only | organizers |
| 14 | Confirm the CFP facts line "one registration covers HCOMP + CI" still stands (the venue-page "jointly badged / early deadline Aug 22" copy was retracted 2026-07-08) | organizers |

## 6. Risks & Mitigations

- **Timeline:** CFP window is now. Ship Phase 0 with placeholder-stamped sections rather than waiting for completeness.
- **Kitsch drift by future maintainers:** STYLE rules live in CLAUDE.md; automated contrast check in a pre-commit or simple CI script; templated YAML + one card component.
- **Fake-archival misstep:** Tier rules in DESIGN.md §7 are launch-blocking, not aspirational.
- **Two-editions confusion:** dual-venue copy rule + ⊕ lockup; review every page's copy against it.
- **Discoverability:** old Google Sites URL is what both conferences link today — repoint + banner.
