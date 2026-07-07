# PRD.md — Nicolas Sanitas: Personal Consulting Site

## 1. What This Is

A personal/professional website for **Nicolas Sanitas**, an AI & Digital Transformation Consultant based in Luxembourg. The site presents his services, career history, expertise, and enables direct booking of consultations via Cal.com.

The design is adapted from the CareerCraft resume builder template, which provides a modern, professional visual identity with Tailwind CSS and a clean component library.

## 2. The Problem

Nicolas has a deployed TanStack Start site (`nicolas-resume.vercel.app`) but needs:
- A more polished, modern design that better reflects his consulting brand
- A clear booking flow for prospects to schedule consultations
- A multilingual front (French, English, German) that works without touching code
- Maintainable content — the static HTML approach allows text changes without a build pipeline

## 3. Target Audience

| User | Profile | What they need |
|------|---------|---------------|
| **C-level executive** | No technical background | Clear, jargon-free explanation of AI services; trust signals (experience, client proof); easy booking |
| **HR/Training manager** | Looking for team upskilling | Evidence of training capability; clear service descriptions; ability to book a discussion |
| **Peer/prospect** | Technical or consulting background | Depth of experience; career history; technical credibility |

## 4. Site Structure

```
Header (sticky)
  ├── Logo: "ns."
  ├── Nav: Services, Career, Approach
  ├── Language toggle: fr / en / de
  └── CTA: Book Consultation

Hero Section
  ├── Badge: AI & Digital Transformation Consultant
  ├── Name + tagline
  ├── CTA buttons: Book Consultation, Download CV
  └── Social links: LinkedIn, WhatsApp

Metrics Strip
  └── 4 key numbers: 20+ years, 50+ orgs, 3 languages, 2 decades shipping

Services Section (3-column grid)
  ├── AI Advisory
  ├── Training Programs
  └── Digital Transformation

Career Timeline
  ├── Exalti (2024–Present)
  ├── Luxinnovation (2021–2024)
  ├── InTech / Groupe POST (2008–2021)
  └── Lux4Good (2015–Present)

Approach Section (3-step process)
  ├── Diagnose
  ├── Decide
  └── Deliver

Foundations Section
  ├── About / bio
  └── Skills tags: Strategic Advisory, AI Literacy, Digital Transformation, etc.

Testimonials
  └── Client quote placeholder

FAQ Section
  └── 4 accordion items

CTA + Booking Section
  ├── "Book a free 20-minute consultation" button
  └── Cal.com embedded scheduling widget (iframe)

Footer
  ├── Logo + tagline
  ├── Services links
  ├── Connect links
  └── Support links

Mobile Bottom Nav (sticky)
  └── Services, Career, Book, FAQ
```

## 5. Content Model

All content is embedded directly in `index.html` as static text. For multilingual support (Phase 2), content would be extracted to JSON files (`en.json`, `fr.json`, `de.json`).

**Key content sections:**
- Hero: name, title, tagline, subtitle, CTA copy
- Metrics: 4 numbers + labels
- Services: 3 cards (title, description)
- Career: 4 entries (company, role, dates, description, bullet points)
- Approach: 3 steps (title, description)
- Foundations: bio text, skills tags
- FAQ: 4 Q&A pairs
- Booking: CTA copy, Cal.com embed URL

## 6. Design & Branding

- **Framework:** Tailwind CSS (CDN), single static HTML
- **Primary color:** Blue (#005ea1) — inherited from CareerCraft
- **Secondary palette:** Blues, grays, neutrals
- **Typography:** Hanken Grotesk (headings), Inter (body)
- **Icons:** Material Symbols Outlined
- **Responsive:** Mobile-first, works at all breakpoints
- **Motion:** Fade/slide-in on scroll for sections

## 7. Non-Functional Requirements

- **Performance:** Single HTML file + CDN assets; fast initial load
- **SEO:** Meta tags for OG, Twitter card, description
- **Accessibility:** Semantic HTML, aria labels on interactive elements
- **Deployment:** Static HTML — deployable to Vercel, Netlify, or any static host
- **Maintainability:** All text in HTML; no build step needed for content changes

## 8. Tech Stack

| Layer | Choice |
|-------|--------|
| Markup | HTML5 |
| Styling | Tailwind CSS (CDN) |
| Icons | Material Symbols Outlined |
| Fonts | Google Fonts (Hanken Grotesk, Inter) |
| Scheduling | Cal.com embed (iframe) |
| Deployment | Vercel / Netlify (static) |

## 9. Future Scope (Out of Scope for V1)

- Multi-language content extraction (JSON files + JS toggle)
- Blog / articles section
- Client testimonials from real clients
- Analytics integration
- Contact form (Tally or similar)
- animated/interactive career timeline

## 10. Related Documents

- `roadmap.md` — phased build plan
- `index.html` — the built site
