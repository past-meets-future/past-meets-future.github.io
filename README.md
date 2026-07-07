# Past Meets Future — workshop website

Static site for the Past Meets Future workshop series (Human-AI Interaction for Digital Humanities & Cultural Heritage).
Current edition: **[/2026/](2026/)** — ACM HCOMP 2026 ⊕ ACM CI 2026, Alexandria VA, Sun Sept 27 2026 · papers due July 30 (AoE).
Live at <https://past-meets-future.github.io/>.

## Working on the site (start here)

Plain hand-written HTML/CSS + one small carousel script. **No build step, no framework, no local server needed** — open the HTML files in a browser, edit, push. Deploy is GitHub Pages deploy-from-branch (`main`) with `.nojekyll`; CSS changes need a `?v=N` bump on the stylesheet links (see MAINTENANCE.md).

Read in this order before changing anything:

1. **[CLAUDE.md](CLAUDE.md)** — working conventions and standing organizer rules. Claude Code loads this automatically; it is the contract.
2. **[DESIGN.md](DESIGN.md)** — the "In Register" brand and design spec: tokens, type, page hierarchy, copy voice, the honest-annotation policy, everything explicitly avoided.
3. **[PLAN.md](PLAN.md)** — verified facts (the single source of truth for site copy), architecture, phases, open items awaiting organizer input.
4. **[MAINTENANCE.md](MAINTENANCE.md)** — task → file map for every routine update (deadline change, accepted papers, keynote, organizers).

## Key rules (full versions in the docs above)

- `2026/data/*.yml` are the **canonical content files** — edit data first, then mirror into the HTML (map in MAINTENANCE.md).
- Past years (`/2024/`, `/2025/`) are **frozen archives. Never edit them.**
- Images: CC0/public-domain only, self-hosted, never hotlinked, never filtered, always credited (colophon carries verbatim rights).
- **Zero em/en dashes in user-facing copy**; schedule says "tentative" until the final program; no unconfirmed logistics claims (early-registration details point to the HCOMP & CI sites).
- Deadline visible three times above the fold; accessibility (WCAG AA, both themes) is content, not polish.

## Agent skills (for Claude Code users)

Skills live in `.agents/skills/` with symlinks in `.claude/skills/`, pinned by `skills-lock.json` — they come with the clone, nothing to install:

- `design-taste-frontend` — anti-slop frontend rules (loaded for any design work)
- `humanizer` — de-slop writing pass (run on every copy change)
- `remotion-best-practices` — for the promo/teaser videos only

To add or update a skill: `npx skills add <owner/repo>`, then move it into `.agents/skills/` and symlink from `.claude/skills/` to match the existing layout.

## Contact

Workshop email: <pastmeetsfuturehaiworkshop@gmail.com> · site issues: open a GitHub issue on this repo.
