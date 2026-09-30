# Noman Hassan portfolio: what to fill in

This site started as a copy of another person's portfolio. The design and code are yours to
reuse. The career sections are now placeholders: fill them with your own facts. Anything in
[square brackets], "Company Name", "Job Title", "X+" or "example.com" is waiting for you.

Already done: your name, "Pakistan", every job marked "Pakistan · Remote", English only (the
language switcher is removed), the old contact details and CV removed.

## Fill in (site content)

| What | File |
|---|---|
| Jobs: company, job title, dates, description (5 entries, "Company Name" / "Job Title") | `src/data/experience.ts` (`ENTRIES` + the `en` block) |
| Education: course and degree ("Course or Bootcamp Name", "University Name") | `src/data/experience.ts`, `index.html` (`alumniOf`, `hasCredential`) |
| About text and "My journey" (the [square bracket] text) | `src/i18n.tsx` (`en` block: `meIntro`, `meJourneyText`) |
| Stats ("X+") | `src/pages/Me.tsx` (`STATS`) |
| Email (placeholder `nomanhassan@example.com`) | `src/pages/Contact.tsx`, `index.html` |
| WhatsApp (placeholder `920000000000`, also drives the QR code) | `src/pages/Contact.tsx`, `index.html` (`telephone`) |
| CV download: add your own `public/Noman-Hassan-CV.pdf` | `public/` |
| Site URL and LinkedIn (`url`, `sameAs`) | `index.html` |
| Projects: 10 Shopify stores + 5 AI case studies with screenshots | `src/data/projects.ts`, `public/projects/` |
| Timeline logos / skills list, if they don't match you | `src/pages/Me.tsx`, `src/pages/Skills.tsx` |

## Delete (the previous owner's personal files, not part of the site)

- `resume/` (CVs and cover letter HTML)
- `ebay/`, `PROPOSAL-GUIDE.md`, `cover/`
- `Noblesse.jpeg`, `noblesse.jpg`, and the design notes `*.md` in the root if you don't need them

## Notes

- `src/i18n.tsx`, `src/data/projects.ts` and `src/data/experience.ts` still contain French,
  Spanish, Italian and German text. The site never shows it (English only). Delete those blocks
  if you want smaller files.
- Run locally: `npm install`, then `npm run dev`, then open http://localhost:5173/portfolio/
- Deploy: push to a GitHub repo named `portfolio`; `.github/workflows/deploy.yml` publishes it to
  GitHub Pages. Change `base` in `vite.config.ts` if the repo has another name.
