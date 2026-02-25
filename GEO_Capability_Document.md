# Generative Engine Optimization (GEO) & Digital Launch Capability Document

**SimplWorks.ai | Cortex | InsurX**
**Established: February 2026**
**Last Updated: February 21, 2026**

---

## Purpose of This Document

This document serves as the origin record and living proof of capability for GEO (Generative Engine Optimization) and full-stack digital launch services delivered by SimplWorks.ai, Cortex, and InsurX. It captures the methodology, deliverables, results, and service framework established through the Top Dog Vending project — the first complete implementation of this service package.

This document will be updated as capabilities expand, new case studies are completed, and the GEO landscape evolves.

---

## What We Do (Client-Facing Language)

Your website will be optimized so that when someone asks ChatGPT, Claude, Perplexity, or Google AI about your business, your information comes up as the answer — not just a link. We don't just get you traffic. We get you quoted.

This is the shift from SEO (Search Engine Optimization) to GEO (Generative Engine Optimization). Traditional SEO gets you ranked in blue links. GEO gets your business cited, summarized, and surfaced as the answer by AI systems that are increasingly how people find businesses.

We bundle GEO into every website build and digital launch package. It's not a separate add-on — it's built into how we construct your digital presence from the ground up.

---

## The GEO Framework: What It Means and Why It Matters

### The Industry Shift

SEO optimized for Google's crawler to win clicks on blue links. GEO optimizes for LLM retrieval and reasoning to win answers, citations, and synthesis.

LLMs don't "search" the way Google does. They retrieve, rank, and compress. They reward:

- Clear entity definitions (who you are, what you do, where you operate)
- Structured explanations (not marketing fluff — direct, quotable statements)
- Explicit relationships ("X does Y for Z in [location]")
- Machine-readable credibility signals (structured data, consistent NAP, authoritative content)

### Two Goals: Cited AND Narrative Control

Getting cited by AI is valuable. But controlling what the AI says about a business is the higher-value play. Our approach does both:

- **Cited**: We structure content so AI systems can find, extract, and reference it accurately.
- **Narrative Control**: We write the exact paragraphs we want AI to extract and repeat — so when someone asks "What is [your business]?" the AI answers with the message we crafted.

### Related Terminology

The industry is still settling on language. Here's how the terms map:

- **GEO (Generative Engine Optimization)** — The emerging standard term. This is what we use.
- **AEO (Answer Engine Optimization)** — SEO practitioners rebranding for AI answers. Same concept, different label.
- **LLMO (LLM Optimization)** — Used in technical/developer circles.
- **AI Search Optimization** — Vague, marketing-friendly version. What we called it before GEO became standard.
- **Semantic SEO** — Transitional term bridging old SEO to GEO.

---

## Proof of Capability: Top Dog Vending Case Study

**Client**: Top Dog Vending (Emory & Ellie)
**Business**: AI-powered smart stores for apartment communities
**Location**: Knoxville, Tennessee
**Timeline**: February 20–21, 2026
**Scope**: Full digital launch — website, SEO, GEO, content marketing, client guides

### Project Deliverables

#### 1. Website Build & Deployment

- Full single-page website built with Next.js and deployed on Vercel
- Mobile-first responsive design with dark theme
- Sections: Hero, About, What Is a Smart Store, See It In Action, How It Works, Benefits, Meet the Owners, Why Top Dog, FAQ, Contact Form
- Contact form connected to Supabase backend for lead capture
- Blog infrastructure with dynamic routing (/blog, /blog/[slug])
- 3 published blog articles targeting property manager search intent
- Professional typography: left-aligned body text, centered headings, 720px max-width containers, 18px desktop font size, WCAG AAA contrast compliance (12.5:1 ratio)

#### 2. Tier 1 — Technical SEO Foundations

- Optimized page title with primary keyword and location
- Meta description leading with zero-cost value proposition (160 chars)
- Full Open Graph tags (title, description, image, URL, site name, locale, type)
- Twitter Card tags (summary_large_image)
- Canonical URL set to production domain
- JSON-LD LocalBusiness structured data (business name, email, service area, service type, founders, image)
- JSON-LD FAQPage structured data (10 FAQ items eligible for Google rich results)
- Auto-generating sitemap.xml (5 URLs)
- Auto-generating robots.txt
- All images optimized via Next.js Image component (WebP/AVIF, responsive srcset, lazy loading, priority loading for hero)
- Semantic HTML (proper heading hierarchy, section/nav/main/footer elements, lang attribute)

#### 3. Tier 2 — Performance & Accessibility

**Lighthouse Scores Achieved:**

| Metric | Desktop | Mobile |
|--------|---------|--------|
| Performance | 100 | 97 |
| Accessibility | 96 | 91 |
| Best Practices | 100 | 100 |
| SEO | 100 | 100 |

**Core Web Vitals (Mobile):**

| Metric | Value |
|--------|-------|
| First Contentful Paint | 1.2s |
| Largest Contentful Paint | 2.0s |
| Total Blocking Time | 10ms |
| Cumulative Layout Shift | 0 |
| Speed Index | 1.9s |

**Key Optimizations:**

- Google Fonts render-blocking fix: Migrated external stylesheet to next/font/google (FCP improved from 2.5s to 1.2s, LCP from 3.0s to 2.0s on mobile)
- WCAG AA/AAA contrast compliance on all text elements
- 5 contextual internal cross-links between page sections
- Mobile verification across all breakpoints (768px, 480px)
- Touch-friendly button sizes (minimum 44px tap targets)

#### 4. Tier 3 — Content Marketing

- Full blog system built with Next.js dynamic routes
- Blog index page, individual article pages with Article JSON-LD schema
- CTA boxes on each article driving to contact form
- All articles included in sitemap

**Articles Published:**

1. "What Is a Smart Store? Everything Property Managers Need to Know" — Educational, targeting concept searches (~600 words)
2. "Smart Store vs. Traditional Vending Machine: What's the Difference?" — Comparison for evaluators (~700 words)
3. "Why Apartment Communities Are Adding Smart Stores in 2026" — Trend piece for decision-makers (~650 words)

#### 5. Tier 4 — Generative Engine Optimization (GEO)

This is the differentiator. Everything above is table stakes. This tier is what makes the business findable and quotable by AI systems.

**AI-Pullable Definition Block:**

Added an entity-rich summary paragraph visible below the hero section containing every key fact about the business in a single crawlable block: company name, location (Knoxville, TN), service description (AI-powered smart stores for apartment communities), product types (fresh food, drinks, snacks, daily essentials), checkout technology (AI-powered, no app, no scanning, no cashier), cost model (zero cost to property), founders' names (Emory and Ellie), and service area (East Tennessee).

This block was specifically designed to be extracted by AI tools (ChatGPT, Claude, Perplexity, Google AI Overview) when answering queries about Top Dog Vending or smart stores in Knoxville. This is narrative control — we wrote the answer we want AI to give.

**FAQ Optimization for AI Extraction:**

- Expanded FAQ from 6 to 10 items
- Every answer rewritten to lead with a direct, quotable first sentence containing entity names and location
- 4 new FAQ items specifically targeting AI assistant queries:
  - "What is a smart store?"
  - "What products can a smart store carry?"
  - "Who is Top Dog Vending?"
  - "How is a smart store different from a vending machine?"

These questions mirror exactly how users query AI systems. The answers are structured so that when an LLM retrieves them, it can extract a clean, accurate response without hallucinating or pulling from competitor sources.

**Structured Data for Machine Understanding:**

- LocalBusiness JSON-LD schema tells AI systems this is a real local business with specific service area, founders, and contact information
- FAQPage JSON-LD schema makes all 10 Q&As directly extractable by both Google and AI systems
- Article JSON-LD on blog posts establishes content authorship and publication context

#### 6. Client Guides & Handoff Documents

- SEO Optimization Report (Feb 20, updated Feb 21) — Complete technical documentation of all SEO/GEO work
- Website Enhancement Report (Feb 21) — Typography, layout, and readability improvements
- Google Business Profile Setup Guide — Step-by-step for client to create GBP listing
- Local Citations Guide — 9 directory listings with copy-paste business description and NAP consistency rules, plus professional email migration steps
- Project To-Do List — Complete status tracker for all remaining deployment tasks

#### 7. Website Design & UX Improvements

- Text alignment overhaul: Center-aligned to left-aligned body text sitewide
- Mobile padding standardized (16px → 24px)
- Step card text hierarchy fixed (left-aligned descriptions, centered icons/titles)
- About section copy restructured from single wall of text to two scannable paragraphs
- Copy improvements: "at zero cost to the property" → "at zero cost to your property" (direct address), reframed from vendor to partner positioning
- Font size consistency: All sections standardized to 18px desktop
- Text contrast: Upgraded from #a0a0a0 to #d1d5db (12.5:1 ratio, exceeds WCAG AAA)

---

## Service Framework

### What's Included in Every Website Build

Every site we build includes the full four-tier optimization as standard. We don't sell GEO as a separate line item — it's how we build.

| Tier | What It Covers |
|------|----------------|
| Tier 1: Technical Foundations | Meta tags, structured data (JSON-LD), Open Graph, sitemap, robots.txt, image optimization, semantic HTML |
| Tier 2: Performance & Accessibility | Core Web Vitals optimization, WCAG compliance, internal linking, mobile verification, render-blocking fixes |
| Tier 3: Content Marketing | Blog infrastructure, SEO-targeted articles, article schema, CTAs |
| Tier 4: GEO | AI-pullable definition blocks, FAQ optimization for AI extraction, entity-rich content, narrative control |

### Post-Launch Services

| Service | Description |
|---------|-------------|
| Managed Hosting | Website hosting, database, monitoring, updates, and fixes |
| Google Workspace Setup | Professional email on client's domain with forwarding configuration |
| Google Business Profile | Setup guide or done-for-you setup |
| Local Citations | Directory listing guide or done-for-you listings |
| Ongoing Content | Additional blog articles, FAQ updates, GEO refinement |

---

## Process Timeline Benchmarks

Based on the Top Dog Vending project (first full implementation):

| Phase | Time |
|-------|------|
| Website build & deployment | ~4 hours |
| Tier 1: Technical SEO foundations | ~1 hour |
| Tier 2: Performance audit + fixes + GBP guide | ~2 hours |
| Tier 3: Blog infrastructure + 3 articles + citations guide | ~3 hours |
| Tier 4: GEO (AI summary, FAQ rewrite, definition block) | ~1 hour |
| Typography, layout, readability polish | ~2 hours |
| Client documents (reports, guides, to-do list) | ~2 hours |
| **Total estimate for a full digital launch** | **~15 hours across 2 days** |

These benchmarks will tighten as the process is repeated. The four-tier SEO/GEO process is documented in the SimplWorks SEO Playbook (`/Users/stephaniebelote/Documents/SimplWorks_SEO_Playbook.pdf`) and codified in the SimplWorks dev stack (`/Users/stephaniebelote/dev-stacks/simplworks.md`).

---

## Client Intake Checklist

What's needed from a new client before starting a build:

### Required
- [ ] Business name (exact legal/brand name to use everywhere)
- [ ] Business location (city, state — full address if local business)
- [ ] Business description (what they do, who they serve, in their words)
- [ ] Owner/founder names and roles
- [ ] Contact email and phone number
- [ ] Photos (logo, product/service photos, team/owner photos — highest resolution available)
- [ ] Domain name (registered or needs to be registered)
- [ ] Target audience (who is the site trying to reach?)

### Helpful but Not Blocking
- [ ] Existing brand colors or preferences
- [ ] Competitor websites they like or want to differentiate from
- [ ] FAQ content (common questions they get from customers)
- [ ] Testimonials or reviews
- [ ] Social media accounts
- [ ] Existing Google Business Profile (if any)

### Post-Build (Client Action Items)
- [ ] DNS access for domain pointing
- [ ] Google Business Profile setup (guide provided)
- [ ] Directory listings (guide provided)
- [ ] Professional email setup (guide provided if applicable)
- [ ] Review and approval of live site

---

## GEO Validation Process

Building for GEO is one thing. Verifying it works is another. Here's how to test:

### Immediate Validation (Day of Launch)
1. **Structured Data Test:** Run the site through Google's Rich Results Test (search.google.com/test/rich-results) — verify LocalBusiness, FAQPage, and Article schemas parse correctly
2. **OG/Twitter Preview:** Use opengraph.xyz or Twitter Card Validator to confirm social sharing previews render correctly
3. **Lighthouse SEO Score:** Must be 100. Anything less means a technical issue needs fixing.

### AI Citation Testing (1–2 Weeks Post-Launch)
1. **Query AI systems directly:**
   - Ask ChatGPT: "What is [business name]?" and "Tell me about [business name] in [city]"
   - Ask Perplexity: Same queries (Perplexity searches live web, so it picks up new content faster)
   - Ask Google AI Overview: Search for the business name and check if the AI overview pulls from the site
2. **Compare the AI's answer to the definition block you wrote.** If the AI is quoting or paraphrasing your definition block, the GEO is working. If it's pulling from other sources or hallucinating, the content may need strengthening.
3. **Test FAQ extraction:** Ask AI systems the exact FAQ questions from the site. Check if the answers match what you wrote.

### Ongoing Monitoring
- Re-test AI queries quarterly as models update their training data and retrieval methods
- Add new FAQ items targeting emerging query patterns
- Publish additional blog content to expand topical authority
- Monitor Google Search Console for impressions and clicks on target queries

---

## Tools & Technology Stack

| Category | Tools |
|----------|-------|
| Development | Next.js, React, CSS (dynamic sites); Static HTML/CSS/JS (simple sites) |
| Deployment | Vercel (Next.js sites); Cloudflare Workers (static HTML sites) |
| Backend/Database | Supabase |
| AI Development | Claude Code (terminal), Claude (strategic/copy), ChatGPT (validation) |
| Performance Testing | Google Lighthouse |
| SEO Validation | Google Search Console, structured data testing |
| Design | Mobile-first responsive, WCAG AAA compliance |

---

## Competitive Advantage

Most web developers and agencies still build for SEO only — optimizing for Google's crawler and blue link rankings. They are not yet building for the AI answer layer.

Our approach is different:

1. **We build for both Google AND AI systems simultaneously.** Every site gets traditional SEO AND GEO from day one.
2. **We write the answer, not just the content.** The AI-pullable definition block is a specific, intentional practice of writing the exact paragraph we want AI systems to extract and repeat.
3. **We optimize for narrative control.** It's not enough to be found — we ensure the AI says the right thing about the business.
4. **We provide complete digital launch packages.** Website + SEO + GEO + content + client guides + email setup + local citations. One provider, everything handled.
5. **GEO is still early.** There is no established playbook. We are building expertise now that will be extremely valuable as demand grows over the next 12–18 months.

---

## Appendix: Origin Project Details

**Project**: Top Dog Vending — Full Digital Launch
**Client**: Emory & Ellie, Knoxville, TN
**Business**: AI-powered Micromart smart stores for apartment communities
**Dates**: February 20–21, 2026
**Live Site**: topdog-website-tau.vercel.app (pending domain: topdogvending.com)
**Status as of Feb 21, 5:00 PM**: Site complete, awaiting client approval and DNS access for domain pointing

**Documents Generated:**

1. SEO Optimization Report (8 pages)
2. Website Enhancement Report (7 pages)
3. Google Business Profile Setup Guide (3 pages)
4. Local Citations Guide (5 pages, includes email migration)
5. Project To-Do List (complete status tracker)

---

---

## Future Case Studies

_Add new case studies here as projects are completed. Copy this template for each new client:_

### Case Study #2: [Client Name]

**Client:** [Name]
**Business:** [What they do]
**Location:** [City, State]
**Timeline:** [Dates]
**Scope:** [What was delivered]

**Results:**
- Lighthouse: Desktop [scores], Mobile [scores]
- GEO validation: [AI citation test results]
- [Any other measurable outcomes]

**Key Deliverables:**
- [List deliverables]

**What Was Different From Previous Projects:**
- [Note anything new, different, or improved in the process]

---

*This document is the property of SimplWorks.ai / Cortex / InsurX. It serves as the foundational capability record for GEO services and will be updated as methodologies evolve and new case studies are completed.*

*SimplWorks.ai — February 21, 2026*
