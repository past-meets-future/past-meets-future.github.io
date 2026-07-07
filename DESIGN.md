# Past Meets Future 2026 — Brand & Design Specification

**Brand: "IN REGISTER"** — *Two plates, one impression.*

Concept No. 3, evolved across three review rounds with the organizers (round 1 "Annotated Catalog" — rejected: Anthropic-coded, Civil-War-centric; round 2 "Under the Lens" — rejected: interaction-first, workshop content buried). Governing directives from those rounds are standing law: **advertise the workshop first; communicate with zero required interaction; represent the whole global, multi-modal field; never Anthropic-coded, never AI-startup-coded.** Live concept: <https://claude.ai/code/artifact/f693eb5a-1e1e-44e3-820d-bf38e46f3e68>

---

## 1. The Brand Story

When two printing plates align perfectly, printers say the impression is **in register** — and the circled-plus registration mark ⊕ is how they check. That is the workshop in one glyph:

**past ⊕ future · human ⊕ AI · HCOMP ⊕ CI — two plates, one impression.**

- **The mark — "seal meets lens" (adopted 2026-07-08, replacing the circled-plus stopgap).** A vermilion seal square, set 7° askew the way a real impression lands, overlapped by a lapis lens circle; where they overlap the ink prints deeper (fill `var(--ink)`: near-black on white, bone on lacquer). The story is native to the site: the vermilion was sampled from the collector seals on *Night-Shining White* (human custodianship), the lapis from the Shahnama's ultramarine (the machine plate); the seal is the human mark on the object, the lens is the machine's attention, and the workshop is the overlap. Same grammar as the detection-box overlays on the collection. Masters in `/shared/brand/` (favicon.svg theme-aware; mark-vermilion/ink/bone are single-ink outline variants); inline instances use `var(--verm)`/`var(--lapis)`/`var(--ink)` with a per-instance clipPath id. **Usage rule (tightened 2026-07-08): exactly ONE placement per page — the nav brand.** The hero venue line is plain text "ACM HCOMP & Collective Intelligence 2026" with no mark between the names (organizer decision: don't get fancy there); never in the milestone bar, never as decoration; the footer lists the conferences as plain links under a "Hosted at" heading (structured footer, 2026-07-08: brand block + three link columns, Workshop / Hosted at / Archive & contact, + a rights line; grid on desktop, two columns at tablet, stacked with taller tap targets on phones). **Standing prohibition (organizer feedback 2026-07-07): nothing crosshair-, target-, or reticle-shaped, ever.** No colophon note for the mark (organizer decision 2026-07-08); it is hand-drawn geometry, not generated imagery.
- **The wordmark** sets PAST / MEETS / FUTURE stacked; PAST carries a slight vermilion plate-offset, FUTURE a lapis one, and they slide *into register* once on page load (pure CSS, ~1.1s, disabled under `prefers-reduced-motion`; final state keeps a 1–2px offset as permanent print character). This is the site's ONLY motion.
- **Two brand inks** carry the two plates:
  - **Vermilion `#C1301C` — the human plate.** Sampled from the collector seals on Han Gan's *Night-Shining White*: twelve centuries of human custodianship stamped in red. Carries deadlines, seal chips, primary CTAs, the PAST plate.
  - **Lapis `#24439B` — the machine plate.** From the Shahnama's ultramarine and Hokusai's Prussian blue. Carries links, data, machine annotations, the FUTURE plate.
- A **Remotion teaser** (social advertising) animates the same brand moment — plates registering over the collection — keeping motion in the ad, not the website.

## 2. Page Hierarchy (the homepage IS an advertisement)

Order is fixed; scholarship is never below decoration:

1. **Milestone bar** — sticky, first HTML kilobyte: current deadline + AoE + "How to submit →". Rotates as the year advances.
2. **Nav** — About · **Call for Participation** (accented) · Dates · Organizers · Venue · Past Editions.
3. **Hero** — kicker ("**The 3rd Annual Workshop** · previously at IUI and ASIS&T" — series continuity above the fold, one line, no № glyphs, years live in Past Editions; organizer feedback 2026-07-07/08) → wordmark → pitch opening "**Human-AI interaction for digital humanities and cultural heritage**" (full workshop scope, never just "meets cultural heritage") and ending "Last year we mapped the field's challenges. **This year we explore solutions, together.**" (never "we build solutions") → plain venue line "ACM HCOMP & Collective Intelligence 2026", both names LINKED, no mark and no fact note beneath (organizer decisions 2026-07-08) → **four fact tiles** (When / Where / **Papers due July 30** / Notifications) → CTA pair.
4. **Task index band** (hero) — breadth in three lines; the imagery moved into §6 as the Solutions Showcase + the **task index band** (transcription ⊕ discovery ⊕ XR·AR·VR ⊕ subject ID ⊕ photographer attribution ⊕ dating ⊕ decipherment ⊕ provenance ⊕ audio ⊕ …).
5. **About** — one paragraph + the two research questions.
6. **From Challenges to Solutions** — the 2026 theme, phrased as EXPLORING solutions and ADDRESSING challenges (organizer feedback 2026-07-07: humanities folks don't frame research as "answers"; acknowledge nothing is solved in one afternoon). The CFP page renders **three** challenge cards (AI-GLAM alignment · cognitive/educational/social impact · ethics) — incentives and IP/copyright/authorship were cut by organizer decision 2026-07-08 — plus the full-width vermilion "the bridge is the method" card (technologists need humanities expertise ⊕ humanities scholarship needs builders/makers; mentoring · collaboration), and the "map is not a checklist" line (topics are never limited to the map). The Miro board is NOT linked publicly (organizer decision 2026-07-07); the mono status line says it is shared with accepted participants.
7. **Call for Participation** — submissions demonstrate interest and relevance (new or old work); solutions are ideated together at the workshop, so never "bring solutions". FOUR formats: A position paper (2-4 pp) · B published paper · C systems & prototypes (working systems, early prototypes, open-source, datasets — presented as lightning talks like all accepted work) · D new modalities (AR/VR/XR; "headsets welcome"). **All four formats visually equal — no "encouraged" emphasis (organizer directive)**. After the formats: the restored **topics-of-interest bullet list** (2024/2025 CFP lineage; the old Metaverse bullet now reads "immersive technologies such as AR, VR, and XR" — the word "Metaverse" is banned, organizer decision 2026-07-08). The intro paragraph does NOT enumerate work types; the format cards do that. The intro is a big tent (2025-CFP tone): name the audiences (HCI, AI, the humanities, GLAM institutions; students; any career stage) and say submissions need not match the challenge map. Facts block: email submission to pastmeetsfuturehaiworkshop@gmail.com by July 30 AoE; single-blind, organizers as PC; one author attends in person; SIGACCESS access line; "unsure whether your work fits? email us and ask".
8. **Key Dates** — ledger; papers due **2026-07-30**; notifications Aug 7; early-bird registration row says "deadline announced on the ACM HCOMP & CI websites" (never a date — organizer decision 2026-07-08); workshop Sept 27.
9. **Schedule** — full-day agenda after the 2024 structure: welcome/intros 9:00 → lightning talks → keynote (TBA) → coffee → small-group affinity mapping → lunch → hands-on sessions I/II with coffee break → report-outs & closing 17:30. Marked **"tentative"** (organizer wording — never "draft") until Aug 7.
10. **Organizers** — six cards; names link to personal sites; each card is exactly TWO lines — role first ("Postdoctoral Fellow, HCI Institute"), institution alone on the second line ("Carnegie Mellon University") — via explicit break, never luck-of-the-wrap. Portraits restored by organizer feedback 2026-07-07: 76px square headshot beside the text, sourced from each organizer's own public page (`photo_source` in `organizers.yml`), grayscale via CSS for cohesion (source files untouched — the never-filter rule is for ARTIFACTS), credited in the colophon.
11. **Venue & Registration** — AB1 Alexandria, Metro, parking, registration fact ("Early-bird registration and its deadline will be announced on the ACM HCOMP 2026 and CI 2026 websites" — the jointly-badged/Aug-22/CrowdCamp copy was retracted 2026-07-08), access line.
12. **Past Editions** — linked ledger: 2024 (Google Sites) · 2025 (Google Sites) · 2026 "you are here". **No future-year rows** (organizer directive: no 2027 mentions).
13. Colophon — full credits, verbatim rights, correction pledge. No design-system meta on the page itself (this document is the system record).

The deadline appears three times above the fold (bar, hot fact tile, CTA). The concept page ships with **zero JavaScript**.

## 3. Color Tokens

| Role | Name | Hex | Contrast | Rules |
| --- | --- | --- | --- | --- |
| Ground (light) | Warm Gallery | `#FBFAF8` | — | One step warm of white (2026-07-08 warmth pass); mats stay pure #FFFFFF so plates read as mounts |
| Text | Overprint Ink | `#16141A` | 18:1 | Where both plates print — all text |
| Human plate | Vermilion | `#C1301C` | 5.7:1 | Deadlines, seals, primary CTA, PAST offset. Fixed hex behind white text in both themes |
| Machine plate | Lapis | `#24439B` | 8.9:1 | Links, data, machine annotation, FUTURE offset |
| Ornament | Manuscript Gold | `#A87B00` | 3.8:1 — fails AA | **Never text.** Hairlines only; dark variant `#E5C15C` may label |
| Ground (dark) | Urushi Lacquer | `#191412` | — | Vermilion-on-lacquer dark mode (`#FF7757`, `#A9BDFF`), not startup dark |
| Dark text | Bone | `#F3EFE9` | 15.9:1 | Never a light-mode ground |

Artifact imagery is never filtered, tinted, or duotoned — true color in both themes.

## 4. Typography (OFL, self-hosted variable subsets ~148KB)

- **Display — Bricolage Grotesque** (800 for wordmark/headlines, uppercase, tight): the poster voice.
- **Text — Archivo**: the institutional record; body, tables, everything organizers edit.
- **Machine voice — Spline Sans Mono**: milestone bar, catalog numbers, rights slugs, status lines, fact labels.

## 5. The Collection (all verified CC0/PD, self-hosted, never hotlinked)

Ten works spanning six continents and four modalities (page/print/textile/stone/sound), each captioned with the human-AI task it represents: Book of the Dead of Nauny (Met, hieroglyph decipherment) · Night-Shining White (Met, provenance & dating) · Ethiopian Illuminated Gospel (Met, Ge'ez transcription) · Shahnama "Feast of Sada" (Met, translation & alignment) · Huexotzinco Codex (LoC, pictograph reading) · Hokusai's Great Wave (Met + AIC, collection discovery) · Wari tunic (Met, pattern analysis; computed palette) · 1906 NY Tribune (LoC, OCR & layout from real ALTO) · **Cosmic Buddha 3D scan (Smithsonian, 3D + AR/VR access via 3d.si.edu)** · **Fisk Jubilee Quartet 1909 (LoC National Jukebox, audio enhancement — waveform computed from the actual recording)**.

Curatorial policy: contested-provenance objects excluded (no Benin bronzes); funerary/sacred contexts named respectfully; never the word "specimen" in user-facing copy; cross-organizer sign-off per object; accession numbers re-verified before launch; correction pledge with one-week SLA in the colophon.

### The Solutions Showcase (compact carousel — replaces the gallery mosaic)

Purpose settled with organizers (2026-07-08 round): the imagery section exists to **showcase what AI can do with heritage material** — the evidence step between the 2025 challenge map and the CFP, and a submission generator. It lives INSIDE the "From Challenges to Solutions" section, not the hero.

Form: one bordered slot (~450px), 11 slides, auto-advancing every 8s with a visible Pause, prev/next, progress line; stops on any interaction; hover pauses; arrow keys work; reduced-motion = manual stepping; no-JS = all slides stacked. Each slide: artifact **with its machine reading visible** (real ALTO OCR boxes, seal outlines, computed palette swatches, computed 1909 waveform) + a two-line story: **"TODAY ·"** (the honest demonstrated capability, vermilion label) and **"IMAGINE ·"** (the wild version, lapis label, italic — person identification across all collections, planet-scale visual search, step-inside-the-temple VR). Speculation is always labeled; demos are always real. Slide 11 is the CTA: "The next reading is yours" → submit by July 30. Slides: Tribune/OCR · Night-Shining White/provenance · papyrus/hieroglyphs · Gospel/subject-and-person ID · codex/pictographs · Shahnama/translation · Great Wave + AIC match/collection discovery · tunic/pattern+palette · Buddha/3D-XR · Fisk waveform/audio · CTA.

## 6. Honest Annotation Policy (launch-blocking)

All captions and marks are task-level and sourced: LoC's own ALTO for the Tribune, computed palettes/waveforms, visible seals and script. **No transcription text ships unless a named expert in that script has verified it.** No AI-generated archival imagery, ever.

## 7. Working Grammar

⊕ mark (logo/lockup/punctuation/focus) · catalog numbers `PMF.26.NNN` · vermilion seal chips (`CFP OPEN`, `EXTENDED`) · reason chips (mono capsules naming the shared task behind any link) · status-line empty states (`AWAITING ACCESSION: accepted papers · Aug 2026`) · milestone bar · task index band with ⊕ separators.

## 8. Yearly Reskin — the Pigment Ledger

Each edition accessions a new collection and samples its accent from the lead object's dominant pigment (darken to ≥4.5:1 on white). 2026 = Vermilion from Night-Shining White. Recorded in a public pigment ledger; next year's announced at the closing session. Past editions freeze at `/2024/ /2025/ /2026/`.

## 9. Pre-Mortem (shipped mitigations)

1. **Buried scholarship** → deadline ×3 above the fold; CFP leads the nav; skip-link to CFP.
2. **Performance collapse** → hotlink ban; fetch→resize→AVIF pipeline; lazy frieze; Lighthouse ≥95 + Slow-4G gate; zero JS.
3. **Colonial vitrine** → written curatorial policy (§5); tasks framed as each tradition's own research problem.
4. **Unverified readings** → §6; named-expert credits.
5. **Maintainer drift** → content in data files, brand components sealed; MAINTENANCE.md task→file map; intentional empty states.
6. **Aging** → the identity is a system (mark, two inks, grammar, ledger), not an effect; re-inks yearly by recipe.

## 9b. Copy Voice (2026-07-08 de-slop pass — standing law)

- **Zero em dashes (—) and en dashes (–) in user-facing copy**, including meta tags, captions, YAML data labels, and table cells. Ranges and compounds use a plain hyphen (`2-4 pp`, `AI-GLAM`, `1863-66`); everywhere else restructure with a comma, colon, period, or the mono `·` separator. A grep for `—|–` across `2026/` must come back clean before shipping.
- **No AI-writing tells**: run the `humanizer` skill (`.claude/skills/humanizer`) over any copy you add or edit — no "not just X but Y", no filler, no forced triads, no "actionable solutions"-style consultant tails.
- **Layout economy**: subpage page titles render on ONE line (the `h1.word span{display:block}` stacking is scoped to the homepage wordmark classes `.w-past`/`.w-fut` only); subpage hero subtitles run wide (`max-width:none`) instead of wrapping at 46ch; proper names ("VT Academic Building One, Alexandria, VA") never break mid-phrase — wrap them in a `white-space:nowrap` span. Don't impose line breaks the copy doesn't need.
- **Claims discipline**: no logistics claims the organizers haven't confirmed (early-reg dates, badging, CrowdCamp coordination, attendance requirements per session). When a fact isn't ours to state, point to the source ("announced on the ACM HCOMP 2026 and CI 2026 websites").

## 10. Explicitly Avoided (standing rules from organizer feedback)

Meta commentary on the live page (concept ribbons, design-system appendices — retired 2026-07-07) · future-year mentions (no "2027") · Anthropic-coded (cream/paper grounds, soft serifs, clay accents, bookish-quiet register) · AI-startup-coded (dark+neon/purple, cyan-on-dark, Space Grotesk/Inter identity, particles, typewriter reveals) · parchment kitsch · required interactivity (nothing essential may depend on hover/click; motion beyond the one wordmark registration needs explicit approval) · US-Civil-War or any single-organizer-project imagery as identity · filters/tints on artifacts · fonts Fraunces, Instrument Serif, Besley, Alegreya · host-venue maroon/orange mimicry.

## Hero Texture — gpt-image-2 prompts (user generates via ChatGPT)

Safety rule: real scripts would render as garbled pseudo-text (forgery-adjacent to this audience) — so the texture must be **deliberately illegible, invented marks**. Keep CSS `opacity ≤ .5` + the fade mask; add a colophon disclosure line when integrated ("background texture: abstract generated ornament, gpt-image-2, deliberately illegible — no real script").

LIGHT (`2026/assets/img/hero-texture-light.jpg`): "A seamless, extremely subtle background texture, landscape 1536x1024: a sparse field of abstract handwritten and inscribed marks suggesting many of the world's writing traditions — brushed strokes, carved lines, cursive fragments, pictographic dashes — all deliberately illegible and invented, belonging to no real language or alphabet. Very pale cool grey marks, no darker than #D9DBDA, on a flat pure white #FFFFFF background. Uniform edge-to-edge density with generous empty space, no focal object, no borders, no recognizable characters, no faces, no pictures, no watermark. Flat, matte, print-like. The texture must be faint enough that black text placed on top remains perfectly readable."

DARK (`-dark.jpg`): same prompt with "very dark warm-grey marks, no lighter than #332C26, on a flat near-black #191412 background… white text placed on top remains perfectly readable."

OG IMAGE (`2026/assets/img/og.jpg`, generate 1216x640 → crop 1200x630): "A bold poster-style social card, landscape 1216x640, flat white #FFFFFF background: the words 'PAST MEETS FUTURE' in huge heavy black #16141A grotesque capitals across the center, with the word 'MEETS' smaller and in vermilion red #C1301C; the letters of 'PAST' show a slight vermilion #C1301C offset shadow up-left, the letters of 'FUTURE' a slight blue #24439B offset shadow up-right, like misregistered printing plates sliding into alignment. Above the title in small dark monospaced capitals exactly: '3RD WORKSHOP ON HUMAN-AI INTERACTION FOR DIGITAL HUMANITIES & CULTURAL HERITAGE'. Below the title in small monospaced capitals exactly: 'ACM HCOMP + CI 2026 · SEPT 27 · ALEXANDRIA VA · PAPERS DUE JULY 30'. In the top left corner a thin vermilion circle-and-crosshair registration mark. All text set exactly once, no other graphics, no watermark." (Proofread every character before shipping; regenerate on any typo.)

## Shipped additions (2026-07-08)
- **Hero featured plate**: Shahnama folio, mat-mounted, rotated −1.6°, catalog tag + credit — fills the right hero column with real CC0 art (never generated imagery). Hidden under 56rem.
- **Brand asset suite** at `/shared/brand/`: mark SVG masters (vermilion/ink/bone), theme-aware `favicon.svg`, favicon-512/32 PNG, apple-touch-icon, wordmark lockups light/dark PNG (browser-rendered from the real fonts).
- Live: <https://past-meets-future.github.io/> · org repo `past-meets-future/past-meets-future.github.io`.

## Accessibility & theming pass (2026-07-08)

- **User theme toggle** on every page: nav pill labeled with the target theme ("Dark mode"/"Light mode"), persisted in localStorage (`pmf-theme`), pre-paint script in <head> prevents flash; stamps `data-theme` on :root over token-level overrides.
- **WCAG fixes**: `<main id="main">` landmark + skip-to-content link on all pages; rotator slides aria-hidden-managed (only active slide exposed); aria-current="page" in nav; touch targets ≥44px on rotator controls; mono microcopy floor raised to .7rem; section rules now Manuscript Gold (decorative only).
- **Warmth dials**: ground #FBFAF8; hero texture opacity .6 with mix-blend multiply (light) / screen (dark) — seamless over any ground.
- **Past editions**: /2024/ and /2025/ redirect instantly to their Google Sites; all in-site past-edition links open in a new tab (rel=noopener).
- CSS cache-busting: bump `?v=N` on every stylesheet edit (see MAINTENANCE.md).
