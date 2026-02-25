# SimplWorks.ai — Development Stack

**Last Updated:** February 25, 2026
**Domain:** simplworks.ai
**Project Location:** `/Users/stephaniebelote/Documents/SimplWorks.ai/`
**GitHub Repo:** StackByStef/simplworks-website
**Status:** Live

---

## What SimplWorks.ai Is

SimplWorks.ai is Stephanie's web design and AI automation agency. Custom-built landing pages and business websites designed for lead capture and conversion. No templates — hand-coded, fast-loading, mobile-first sites.

**Services:**
- Custom landing pages
- Business websites
- Lead capture forms wired to real databases
- Email signup systems
- Domain + deployment setup
- Mobile-first responsive design

**Target markets:** Startups, small businesses, podcasts/creators, service providers

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Architecture** | Static HTML/CSS/JS + Cloudflare Worker handler for API |
| **Styling** | Pure CSS (CSS custom properties / inline `<style>` tags) |
| **Fonts** | Google Fonts — Instrument Serif (headlines), DM Sans (body) |
| **Color Scheme** | Dark mode (#0a0a0a bg, #f5f2ed text, #4f8cff accent blue, #ebe6dd cream) |
| **Hosting** | Cloudflare Workers (`simplworks-ai` worker) |
| **DNS** | Cloudflare |
| **Domain Registrar** | Namecheap |

---

## API Platforms & Services

### Supabase — Lead Capture
- **Same project as Cortex:** eyqhnijwanhhxzitkyhn
- **Table:** `strategy_call_leads`
- **Fields:** name, email, phone, business, message, source
- **Integration:** Direct REST API calls via fetch (no SDK)
- **Used for:** "Book a Strategy Call" form on landing page

### Cloudflare Workers — Hosting + API
- **Main worker:** `simplworks-ai`
- **Worker handler:** `src/index.js` — serves `/api/contact` POST endpoint (writes to Supabase), everything else falls through to static assets
- **Redirect worker:** `simplworks-www-redirect` (301 www → non-www)
- **Config:** `wrangler.jsonc` in project root
- **Compatibility date:** 2026-02-06
- **Entry point:** `./src/index.js`
- **Assets directory:** `./public` (bound as `ASSETS`, `run_worker_first` for `/api/*`)

---

## Website Sections (Single Page)

1. **Nav Bar** — Logo, Services, Process, Industries, About, "Get Started" CTA
2. **Hero** — "Landing pages that actually convert."
3. **Services** — 6-card grid (Landing Pages, Business Websites, Lead Capture Forms, Email Signups, Domain + Deployment, Mobile-First Design)
4. **Process** — 3 steps: Map → Build → Deploy
5. **Industries** — 2x2 grid (Startups, Small Businesses, Podcasts/Creators, Service Providers)
6. **About** — Founder bio, stats cards (Hand-Coded, Fast Turnaround, 100% Responsive, 0 Templates)
7. **Contact** — Strategy call form + contact info
8. **Footer** — Copyright 2026

---

## Contact & Business

- **Email:** stephanie@simplworks.ai
- **Phone:** 678.617.4598
- **Lead capture:** All form submissions → Supabase `strategy_call_leads` table
- **Analytics:** None currently configured

---

## File Structure

```
/Users/stephaniebelote/Documents/SimplWorks.ai/
├── index.html                              # Legacy root index (631 lines, original version)
├── wrangler.jsonc                          # Cloudflare Workers config
├── .gitignore                              # Excludes .netlify
├── src/
│   └── index.js                            # Worker handler (API endpoint + asset serving)
├── public/
│   └── index.html                          # Primary site file (1,119 lines — redesigned)
├── Cortex_Website_Build_Master_Playbook.md # Build/deployment procedures
├── GEO_Capability_Document.md              # GEO targeting capabilities
├── SimplWorks_Website_Build_Playbook.md    # Website build process
├── SimplWorks_SEO_Playbook.pdf             # SEO optimization framework
├── simplworks-dev-stack.md                 # Local dev stack documentation
├── SW_*.txt / orphan_copy_*.txt            # Website copy variations (Feb 22-24)
├── Site_Frame.html                         # Site frame mockup
└── .netlify/                               # Legacy config (no longer used)
```

---

## Migration History

- **Feb 3, 2026:** Initial landing page created and deployed to Netlify
- **Feb 6, 2026:** Migrated from Netlify to Cloudflare Workers (Netlify locked due to free tier limits)
- **Feb 8, 2026:** `simplworks-www-redirect` worker deployed (fixes broken www link in email signature)
- **Feb 22-24, 2026:** Full website redesign — new copy, new fonts (Instrument Serif + DM Sans), new color palette (#f5f2ed cream text), server-side form handler added (`src/index.js`)
- **Feb 25, 2026:** Redeployed to Cloudflare Workers with current version

---

## Standard Client Website Process — SEO Optimization

**MANDATORY for every website SimplWorks builds.** No exceptions. First deployed on Top Dog Vending (Feb 20, 2026).

**Full playbook PDF:** `/Users/stephaniebelote/Documents/SimplWorks_SEO_Playbook.pdf`

### Tier 1: Technical Foundations (before launch)
- Page title + meta description (50-60 chars / 150-160 chars)
- Open Graph tags + Twitter cards (og:title, og:description, og:image)
- Canonical URL set to production domain
- JSON-LD structured data: LocalBusiness (for local businesses) + FAQPage (if FAQ exists)
- Auto-generating sitemap.xml and robots.txt
- All images through next/image (WebP/AVIF, responsive srcset, lazy loading, descriptive alt text)
- Semantic HTML (proper heading hierarchy, section/article/main elements)

### Tier 2: Performance & Accessibility (first week)
- Run Lighthouse audit (mobile + desktop) — target 90+ all categories, 100 SEO
- Eliminate render-blocking resources (next/font instead of Google Fonts link)
- Fix WCAG AA contrast issues (4.5:1 normal text, 3:1 large text)
- Internal cross-linking between page sections
- Google Business Profile setup guide (PDF for client, local businesses only)
- Mobile verification via Lighthouse

### Tier 3: Content Marketing (weeks 2-4)
- Blog with 3+ SEO-targeted articles (1 educational, 1 comparison, 1 trend/benefit)
- Each article: proper meta, OG, Article schema, internal links, CTA box
- Blog added to nav, footer, sitemap
- Local citations guide (PDF for client, local businesses only)

### Tier 4: AI Search Optimization / GEO (ongoing)
- FAQ answers rewritten to lead with direct, quotable 1-sentence statements
- New FAQ items targeting AI assistant queries ("What is X?", "Who is X?", "How does X work?")
- AI-pullable definition block (entity-rich summary paragraph, visible on page)
- Service area pages (if client expands geography)

### Client Handoff Deliverables
- SEO optimization report (PDF documenting everything done)
- Google Business Profile setup guide (PDF)
- Local citations guide (PDF)
- All three stored in the client's project folder

### First Use
- **Client:** Top Dog Vending (Emory & Ellie)
- **Date:** February 20, 2026
- **Results:** Desktop 100/100, Mobile 97/100, SEO 100/100
- **Report:** `/Users/stephaniebelote/Documents/Top Dog Vending/SEO_Optimization_Report.pdf`

---

## How to Deploy

```bash
cd /Users/stephaniebelote/Documents/SimplWorks.ai
CLOUDFLARE_API_TOKEN=5bt6zDWYKkW4o4REJ9vtEpW3RuYHoEa_QQlVFbfZ npx wrangler deploy
```
