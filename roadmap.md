# roadmap.md — Sheela Gowda: Site Roadmap

---

## Phase 0 — Static Landing Page (COMPLETE)

**Goal:** A visually complete, deployable single-page site with all content and booking integration.

**Done:**
- [x] Single `index.html` using Tailwind CSS (CDN) + CareerCraft design template
- [x] Hero section with name, tagline, CTA buttons, social links
- [x] Metrics strip (20+ years, 50+ orgs, 3 languages, 2 decades)
- [x] Services section (AI Advisory, Training, Digital Transformation)
- [x] Career timeline (Exalti, Luxinnovation, InTech/POST, Lux4Good)
- [x] Approach section (Diagnose, Decide, Deliver)
- [x] Foundations/bio section with skills tags
- [x] Testimonials placeholder
- [x] FAQ accordion (4 items)
- [x] Booking CTA + Cal.com embed (iframe)
- [x] Footer with all links
- [x] Mobile responsive + sticky bottom nav
- [x] SEO meta tags (OG, Twitter, description)
- [x] Scroll animations

---

## Phase 0.5 — Polish & Hardening (Next 2 Hours)

**Goal:** Fix rough edges before publication.

| Item | Why it matters |
|------|---------------|
| **1. Replace Cal.com placeholder URL** with actual Cal.com account link | Booking won't work until the real Cal.com link is configured |
| **2. Create a real CV PDF** at `/cv-sheela-gowda.pdf` | Download button currently has no file to serve |
| **3. Add real client testimonials** — replace placeholder quote with actual feedback | Social proof is critical for consulting trust |
| **4. Review and finalize copy** — proofread all sections | Professional polish |
| **5. Add favicon** — replace the SVG emoji with a real icon | Browser tab branding |

---

## Phase 1 — Multilingual Support (This Week)

**Goal:** Site content available in French, English, and German without editing HTML.

| Item | Dependencies |
|------|-------------|
| **Extract content to JSON files** — `en.json`, `fr.json`, `de.json` with all site text | None |
| **Language switcher logic** — JS that reads JSON and swaps text on toggle | JSON files |
| **Persist language choice** — store in localStorage, default to browser language | Language switcher |
| **Handle Cal.com in multilingual context** — link to language-specific Cal.com pages if available | Cal.com account setup |

---

## Phase 2 — Engagement Features (Next Week)

**Goal:** Increase conversion and user engagement.

| Item | Notes |
|------|-------|
| **Tally or similar contact form** — for prospects who prefer email over booking | Lightweight embed, same as Why Lab approach |
| **Analytics** — privacy-focused (Plausible or Umami) | Understand which sections drive bookings |
| **PDF auto-generation** — for CV or service brochures | Possibly client-side using a library |
| **Blog / articles section** — thought leadership content | Positions you as an authority |

---

## Phase 3 — App Migration (If Needed)

**Goal:** Migrate from static HTML to a framework if dynamic features require it.

| Item | Notes |
|------|-------|
| Evaluate static HTML vs. framework (TanStack Start or Astro) | Needed if more than ~5 pages or if CMS integration required |
| Headless CMS integration (Sanity or Strapi) | If you want non-technical content editing |
| Server-side PDF generation | For dynamic CV or brochure generation |

---

## Open Decisions

| Decision | Blocks |
|----------|--------|
| Cal.com account setup | Phase 0.5 item #1 — booking is non-functional without real Cal.com link |
| Real CV PDF location | Phase 0.5 item #2 |
| Analytics tool choice (Plausible vs. Umami vs. Google) | Phase 2 — analytics |
| Blog content strategy | Phase 2 — blog section |
| Multilingual approach (manual JSON vs. i18n library) | Phase 1 |

---

## Related Documents

- `prd.md` — full product description
- `index.html` — the built landing page
