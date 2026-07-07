# Maintenance map — every yearly task, by file and place

| Task | Edit |
|---|---|
| CSS edits | Bump the `?v=N` query on the stylesheet link in all four index.html files (GitHub Pages caches CSS for 10 min; browsers longer) |
| Deadline / date change | `2026/data/dates.yml`, then: milestone bar (top of ALL four pages), homepage fact tiles, CFP facts block + Key Dates table (`2026/cfp/`), attend-page hero line, `2026/pmf2026.ics` |
| Early registration | NO date on our site until the conference sites publish one — the approved line everywhere is "Early-bird registration and its deadline will be announced on the ACM HCOMP 2026 and CI 2026 websites" |
| Keynote announced | `2026/data/schedule.yml` + Schedule table row "Keynote" (remove TBA chip) |
| Accepted papers (after Aug 7) | `2026/data/papers.yml` + new "Accepted Works" section (copy the Key Dates section pattern); PDFs into `2026/assets/papers/` — never personal Drive links |
| Organizer change | `2026/data/organizers.yml` (fields: `name`, `role`, `institution`, `url`) + Organizers section. Cards are exactly TWO lines: role first, institution alone on the second (explicit `<br>`). No headshots |
| Schedule change | `2026/data/schedule.yml` + Schedule table on `2026/attend/`. Header says "tentative" until the final program lands (Aug 7) — never "draft" |
| Miro board | Challenges section link. Owner must keep share link VIEW-ONLY; for permanence export challenge frames to PDF/PNG into `2026/assets/` and link that too |
| Hero background texture | Generate with gpt-image-2 (prompts in DESIGN.md §Hero texture), save as `2026/assets/img/hero-texture-light.jpg` (+ `-dark.jpg`), swap in `.hero-bg` CSS (marked comment), keep opacity ≤ .5 + fade mask; add a colophon line "background texture: abstract generated ornament (gpt-image-2), deliberately illegible, no real script" |
| og:image | Compose 1200×630 from the wordmark + fact tiles; save `2026/assets/img/og.jpg`; uncomment meta tag |
| Post-workshop | Freeze `/2026/`; next year copies the folder pattern |

Rules that must never regress: deadline visible 3× above the fold · no AI-generated archival imagery · every image credited with verbatim rights · WCAG AA on both themes · showcase carousel has Pause and stops on interaction · zero em/en dashes in user-facing copy (grep `—|–` across `2026/` before shipping; run the `humanizer` skill on copy changes) · no unconfirmed logistics claims (early registration always points to the HCOMP & CI sites).
