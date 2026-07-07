# Maintenance map — every yearly task, by file and place

| Task | Edit |
|---|---|
| CSS edits | Bump the `?v=N` query on the stylesheet link in all four index.html files (GitHub Pages caches CSS for 10 min; browsers longer) |
| Deadline / date change | `2026/data/dates.yml`, then `2026/index.html`: milestone bar (top), fact tile "Papers due", CFP facts block, Key Dates table, `2026/pmf2026.ics` |
| Keynote announced | `2026/data/schedule.yml` + Schedule table row "Keynote" (remove TBA chip) |
| Accepted papers (after Aug 7) | `2026/data/papers.yml` + new "Accepted Works" section (copy the Key Dates section pattern); PDFs into `2026/assets/papers/` — never personal Drive links |
| Organizer change | `2026/data/organizers.yml` + Organizers section (names + affiliations only, no headshots) |
| Miro board | Challenges section link. Owner must keep share link VIEW-ONLY; for permanence export challenge frames to PDF/PNG into `2026/assets/` and link that too |
| Hero background texture | Generate with gpt-image-2 (prompts in DESIGN.md §Hero texture), save as `2026/assets/img/hero-texture-light.jpg` (+ `-dark.jpg`), swap in `.hero-bg` CSS (marked comment), keep opacity ≤ .5 + fade mask; add a colophon line "background texture: abstract generated ornament (gpt-image-2), deliberately illegible, no real script" |
| og:image | Compose 1200×630 from the wordmark + fact tiles; save `2026/assets/img/og.jpg`; uncomment meta tag |
| Post-workshop | Freeze `/2026/`; next year copies the folder pattern |

Rules that must never regress: deadline visible 3× above the fold · no AI-generated archival imagery · every image credited with verbatim rights · WCAG AA on both themes · showcase carousel has Pause and stops on interaction.
