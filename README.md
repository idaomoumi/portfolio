# Ida Omoumi — Cybersecurity Portfolio

A personal portfolio site for Ida Omoumi, Cybersecurity Consultant (M.S. Cybersecurity, ISC2 CC), built around her real client-facing work in incident response, IAM, and security assessments.

## Overview

- **Stack:** Next.js 14 (App Router), TypeScript, Tailwind CSS
- **Design direction:** Dark, SOC-inspired aesthetic. Instead of a generic "dashboard with fake charts" hero, the signature visual is a terminal-style status log, and the featured-work section presents real engagements as redacted incident tickets (case ID, severity, status, outcome) — a layout that mirrors how Ida actually works a case.
- **Content:** Every section is built from her resume — no invented metrics or fabricated outcomes. A couple of spots in the code are good candidates for a real number if you have one on hand (e.g., number of clients served, exact migration size); search for `CASE-` entries in `components/FeaturedWork.tsx` if you want to tighten those further.

## Project Structure

```
ida-portfolio/
├── app/
│   ├── layout.tsx        # Root layout, fonts, metadata
│   ├── page.tsx          # Assembles all sections
│   └── globals.css       # Tailwind + custom utilities (grid texture, blink/scan animations)
├── components/
│   ├── NavBar.tsx         # Sticky nav with mobile menu
│   ├── Hero.tsx           # Hero + animated "status log" signature element
│   ├── About.tsx
│   ├── CoreExpertise.tsx  # 6 expertise areas
│   ├── FeaturedWork.tsx   # 3 cases styled as incident tickets
│   ├── Experience.tsx     # Timeline
│   ├── Credentials.tsx    # Education + certifications
│   ├── Skills.tsx         # Categorized technical skills
│   ├── Research.tsx       # Research, CTF mentoring, pro bono work
│   ├── Contact.tsx
│   ├── Footer.tsx
│   └── SectionTag.tsx     # Shared numbered section label
├── tailwind.config.ts     # Custom color tokens (ink/panel/signal/amber) and animations
├── next.config.js
├── tsconfig.json
└── package.json
```

## Local Setup

```bash
npm install
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000).

To build for production:

```bash
npm run build
npm start
```

No environment variables or external services are required.

## Editing Content

All copy lives directly in the component files under `components/` — there's no CMS or data layer. To update a section, edit the relevant array or JSX directly (e.g., job history is in `Experience.tsx`, skills are categorized in `Skills.tsx`).
