# Inua Nurse Footprint (INF) — Website README

> **Organisation:** Inua Nurse Footprint (INF) Website
>
> **Purpose:** Public-facing website for INF to showcase mission, activities, events, partners, accept donations & volunteers, share resources, and grow the INF community across universities and the continent.

---

## Table of contents

1. Home
2. Core features & pages
3. Tech stack & architecture (recommended)
4. Project structure (suggested)
5. Installation & development
6. Deployment
7. Content & data requirements
8. Design and branding notes
9. Forms & integrations
10. Accessibility, SEO & analytics
11. Security & privacy
12. Contribution guide
13. Contact
14. Gallery

---

## 1. HOME

This repository contains the code and documentation for the official **Inua Nurse Footprint (INF)** website. The site is intended for:

* Sharing INF’s mission, vision, objectives and impact.
* Announcing upcoming events, training and medical camps.
* Recruiting volunteers and mentors (mentor–mentee signups).
* Accepting donations and managing donor acknowledgements.
* Publishing resources, reports, and research outcomes.
* Displaying partners and ways to collaborate.

## 2. Core features & pages

**Primary pages**

* Home (hero, latest news, quick actions)
* About (mission, vision, objectives, team, history)
* Programs (mentorship, training, outreach, research)
* Events (calendar, register for events)
* Impact (stories, reports, metrics)
* Partners & Donors (logos, contact CTA)
* Get Involved (volunteer, mentorship sign-up, student chapters)
* Donate (payment integration, donor tiers)
* Blog / News (articles, press releases)
* Resources (downloads: proposals, research, toolkits)
* Contact (contact form, office address, socials)
* Privacy & Terms

**Utility & admin**

* Admin dashboard (manage events, posts, volunteers)
* CMS or markdown-based content (editable by communications team)
* Newsletter signup & mailing list integration

## 3. Tech stack & architecture (recommended)

**Frontend**

* React (Next.js recommended for SSR & SEO)
* TailwindCSS for styling (consistent with prior design guidance)
* TypeScript (recommended)

**Backend / CMS**

* Headless CMS: Sanity / Strapi / Netlify CMS / Contentful (choose depending on budget)
* Serverless functions (for forms, webhooks)

**Payments & Forms**

* Stripe (payments & donation flows)
* PayPal (optional)
* Use serverless endpoints for secure processing

**Hosting & deployment**

* Vercel (preferred for Next.js) or Netlify
* GitHub for code repo and CI

**Optional**

* Database: Firebase / Supabase / PostgreSQL (for volunteers, registrations)
* Email: Mailgun / SendGrid
* Analytics: Google Analytics / Plausible

## 4. Project structure (suggested)

```
/ (repo root)
├─ public/                     # static assets, images, logo
├─ src/
│  ├─ components/              # reusable UI components
│  ├─ pages/                   # Next.js pages or routes
│  ├─ styles/                  # Tailwind config + global styles
│  ├─ lib/                     # helpers, API clients
│  ├─ data/                    # local content or sample JSON
│  └─ admin/                   # admin CMS (if using Netlify CMS)
├─ scripts/                    # deployment or migration scripts
├─ .env.example                # environment variable template
├─ README.md                   # this file
└─ package.json
```

## 5. Installation & development

**Prerequisites:** Node.js (16+), npm or yarn, Git

```bash
# Clone repo
git clone https://github.com/<org>/inf-website.git
cd inf-website

# Install
npm install
# or
# yarn

# Development (Next.js)
npm run dev
# Build
npm run build
# Start
npm run start
```

**Environment variables** (example `.env.local`)

```
NEXT_PUBLIC_SITE_NAME="Inua Nurse Footprint"
NEXT_PUBLIC_BASE_URL="https://inf.org" # replace with real URL
NEXT_PUBLIC_ANALYTICS_ID=""
STRIPE_SECRET_KEY=""
STRIPE_PUBLISHABLE_KEY=""
CMS_API_KEY=""
EMAIL_SERVICE_API_KEY=""
```

## 6. Deployment

**Vercel (recommended)**

* Connect GitHub repo to Vercel.
* Add environment variables in the Vercel dashboard.
* Set production branch (main) and enable automatic deploys.

**Netlify**

* Connect repo, set build command: `npm run build` and publish directory for static exports.

**Best practices**

* Use preview branches for content team QA.
* Protect production branch with PR reviews.

## 7. Content & data requirements

Prepare the following content for launch:

* High-res logo (SVG + PNG)
* Brand color codes (see Design & Branding below)
* Short and long site descriptions (for meta and About page)
* Team bios and headshots
* Program descriptions and SOPs
* Donation tiers, bank/account details, NGO registration docs
* Sample event data (title, description, venue, date, registration link)
* Resource PDF files (proposals, reports)

## 8. Design and branding notes

**Primary color palette** (INF requested)

* Dark Blue: use as primary brand color for header/footer and CTAs
* White: background and text contrast

**Typography**

* Clear, legible fonts — use system stack or Google Fonts (e.g., Inter, Poppins)

**Tone**

* Mix professional & approachable: use formal language for reports, friendlier tone for calls-to-action.

**Imagery**

* Use photos from events (medical camps, trainings) with consent.
* Use simple illustrations for campaigns; consider cartoon-style front and back covers for printable materials.

**Accessibility**

* Ensure color contrast, skip-links, alt text for images, and keyboard navigation.

## 9. Forms & integrations

**Key forms**

* Volunteer / Mentor sign-up (name, institution, year, skills, availability, phone, email)
* Event registration (name, institution, contact, fees if applicable)
* Contact form (message routing to support email)
* Donation form (Stripe integration)
* Partner interest / sponsorship form

**Integrations**

* Email (SendGrid / Mailgun) for transactional emails
* Payment gateway (Stripe with webhooks)
* Google Calendar or Calendar API for events
* CRM / Airtable / Google Sheets as lightweight data store for sign-ups

## 10. Accessibility, SEO & analytics

**SEO**

* Proper meta titles & descriptions for all pages
* Open Graph tags for sharing (image, title, description)
* Sitemaps & robots.txt

**Analytics**

* Google Analytics / Plausible for traffic
* Track donation conversions and event signups

**Accessibility**

* WCAG AA as baseline
* Use semantic HTML, aria-* attributes where needed

## 11. Security & privacy

* Do not store card details on the site; use Stripe
* Secure serverless endpoints and validate inputs
* Provide a clear Privacy Policy and Terms of Use
* Encrypt environment secrets in hosting platform

## 12. Contribution guide

**How to contribute**

1. Fork repo and create a feature branch: `feature/your-change`
2. Make changes and add tests where necessary
3. Open a Pull Request with a clear description
4. Team lead or tech maintainer will review and merge

**Coding standards**

* Use Prettier & ESLint (config included)
* Commit messages should be clear and reference issue IDs when applicable

## 13. Contact

Organisation lead / owner:
**Israel Alex Makori**
President, Inua Nurse Footprint (INF)
Chairperson, Nairobi University Nursing Students Association (NUNSA)
Email: [inf.go.ke@gmail.com](mailto:inf.go.ke@gmail.com)
Phone: +254 112569560

---

### Notes & Next steps

* If you want, we can scaffold a Next.js starter repo (with Tailwind, sample pages, and forms) and a simple Contentful/Sanity schema for INF content.
* Provide logos, preferred domain, and payment account details so we can wire up real donation flows.
* If you prefer a simpler static site, we can prepare a vanilla React or Gatsby starter instead.

---

*README generated for INF by ChatGPT — edit as needed.*
