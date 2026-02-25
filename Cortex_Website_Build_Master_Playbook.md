# Cortex Website Build Master Playbook

**Cortex Internal Reference — SimplWorks.ai Client Website Builds**
**Created: February 22, 2026**
**Last Updated: February 22, 2026**
**Prototype Project: Top Dog Vending (topdogvending.com) — February 20-21, 2026**
**Location: `/Users/stephaniebelote/cortex-memory-logger/Cortex_Website_Build_Master_Playbook.md`**

---

## How to Use This Document

**Cortex: Read this document at the start of every new client website project.** This is the master reference for how SimplWorks builds websites. Every design decision, every SEO checklist item, every deployment step is here. Follow it. Don't deviate unless Stephanie explicitly asks for something different.

Top Dog Vending was the prototype. Everything in this playbook was proven on that build. The standards here are the minimum — beat them if you can.

**Related documents (do NOT confuse with this one):**
- `GEO_Capability_Document.md` — Proves what we can do (client-facing capability record)
- `simplworks-dev-stack.md` — Documents SimplWorks.ai's own website tech stack
- `SimplWorks_SEO_Playbook.pdf` — Original SEO tier framework (this playbook supersedes it)
- `CORTEX_CORE_IDENTITY.md` — Stephanie's identity file (biographical facts, corrections)

---

## Design Standards

These are non-negotiable. Every site follows these rules. They were established on Top Dog Vending and are the reason that site looks professional.

### Typography

| Element | Rule |
|---------|------|
| **Body font size** | 18px on desktop, 16px on mobile |
| **Body font** | Inter (for static HTML sites) or Montserrat (for Next.js sites). Never DM Sans. |
| **Heading font** | Space Grotesk |
| **Line height** | 1.7 for body text, 1.15-1.3 for headings |
| **Max content width** | 720-780px for body text paragraphs |
| **Max section width** | 1100px |
| **Font loading** | next/font/google (Next.js) or preconnect + display=swap (static). NEVER external stylesheet link without preconnect — it causes render-blocking. |
| **Font smoothing** | `-webkit-font-smoothing: antialiased` on body |

### Text Alignment

| Element | Alignment |
|---------|-----------|
| **Section headings** | Centered |
| **Section subtitles** | Centered |
| **Section tag labels** (e.g., "What We Build") | Centered |
| **Body text paragraphs** | Left-aligned within centered containers |
| **Card titles** | Left-aligned (or centered if card is centered layout like process steps) |
| **Card descriptions** | Left-aligned |
| **Hero content** | Centered |

This means section headers get wrapped in a centered container (`.section-header` with `text-align: center; max-width: 780px; margin: 0 auto 60px;`) and the body content below is left-aligned.

### Color System

| Element | Value | Notes |
|---------|-------|-------|
| **Background (main)** | `#0a0a0a` | Near-black |
| **Background (alt)** | `#111111` | Slightly lighter, for variety |
| **Background (cards)** | `#161616` | Visible against main bg. NOT transparent/rgba. |
| **Text (primary)** | `#d1d5db` | WCAG AAA compliant (12.5:1 ratio). NOT #888 or #777. |
| **Text (dim/muted)** | `#9ca3af` | For subtitles, secondary text |
| **Text (headings)** | `#f0f0f0` | Near-white for maximum contrast |
| **Accent color** | Per brand. Top Dog: `#FF8200`. SimplWorks: `#4f8cff`. |
| **Accent hover** | Slightly darker version of accent |
| **Accent glow** | Accent at 15% opacity, for icon backgrounds |
| **Borders** | `rgba(255, 255, 255, 0.06)` | Subtle dividers |
| **Border hover** | Accent at 30-40% opacity | Blue/orange glow on hover |
| **Dividers** | `rgba(255, 255, 255, 0.06)` | Between sections |

**WCAG Compliance:** All body text must pass WCAG AA minimum (4.5:1 contrast ratio). Target AAA (7:1) where possible. The `#d1d5db` on `#0a0a0a` combination achieves 12.5:1 — use this as the standard.

### Card Design

| Property | Value |
|----------|-------|
| **Background** | `#161616` (solid, not transparent) |
| **Border** | 1px solid `rgba(255, 255, 255, 0.06)` |
| **Border radius** | 14px |
| **Padding** | 36px 28px (large cards), 24px (small cards) |
| **Hover effect** | Border color changes to accent glow + `translateY(-3px)` |
| **Transition** | `border-color 0.3s, transform 0.3s` |

### Layout & Spacing

| Element | Value |
|---------|-------|
| **Nav height** | 72px, fixed position |
| **Nav background** | `rgba(10, 10, 10, 0.92)` with `backdrop-filter: blur(12px)` |
| **Section padding** | 100px top/bottom on desktop, 60px on mobile |
| **Side padding** | 40px desktop, 24px mobile |
| **Scroll behavior** | `smooth` with `scroll-padding-top: 80px` (clears fixed nav) |
| **Card grid gap** | 24px (standard), 32px (process steps) |

### Icons

- Use emoji for "Who We Serve" vertical cards (rocket, building, microphone, briefcase)
- Use Unicode symbols for service cards (varied, not all the same diamond)
- Icons sit inside 44x44px containers with `border-radius: 10px` and accent glow background

### Responsive Breakpoints

| Breakpoint | Changes |
|------------|---------|
| **768px** | Hide desktop nav, single-column grids, reduce section padding to 60px, reduce font to 16px |
| **480px** | Smaller headings, stack hero buttons vertically |

### Buttons

| Type | Style |
|------|-------|
| **Primary CTA** | Accent color background, white text, 14px 36px padding, 8px radius, 600 weight |
| **Secondary CTA** | Transparent background, text color, 1px border, same padding/radius |
| **Hover** | Primary darkens + translateY(-2px). Secondary border brightens. |

---

## Four-Tier SEO/GEO Process

Every website gets all four tiers. This is not optional. It's how we build.

### Tier 1: Technical Foundations (Before Launch)

**Must be complete before the site goes live.**

- [ ] Page title: 50-60 characters, primary keyword + location (if local business)
- [ ] Meta description: 150-160 characters, lead with value proposition
- [ ] Open Graph tags: og:title, og:description, og:image, og:url, og:site_name, og:locale, og:type
- [ ] Twitter Card tags: card type (summary_large_image), title, description, image
- [ ] Canonical URL set to production domain
- [ ] JSON-LD LocalBusiness schema (for local businesses): name, email, service area, service type, founders, image
- [ ] JSON-LD FAQPage schema (if FAQ section exists): all Q&As
- [ ] Sitemap.xml — auto-generating or manually created, all pages included
- [ ] Robots.txt — allow all, reference sitemap
- [ ] All images optimized: WebP/AVIF format, responsive srcset, lazy loading, descriptive alt text, priority loading for hero/above-fold
- [ ] Semantic HTML: proper heading hierarchy (one h1, h2s for sections, h3s for cards), section/article/main/footer elements, lang attribute on html tag

**For Next.js sites:** Use Next.js metadata API and next/image component. These handle most of this automatically.

**For static HTML sites:** Add all meta tags manually in `<head>`. Use `<img>` with width/height attributes and loading="lazy".

### Tier 2: Performance & Accessibility (First Week)

**Must be verified within one week of launch.**

- [ ] Run Lighthouse audit (mobile + desktop)
- [ ] **Target scores:** Performance 90+, Accessibility 90+, Best Practices 100, SEO 100
- [ ] Eliminate render-blocking resources (fonts are the #1 offender — use next/font or preconnect+swap)
- [ ] WCAG AA contrast on all text (4.5:1 normal, 3:1 large). Target AAA where possible.
- [ ] Internal cross-linking between page sections (minimum 5 links)
- [ ] Mobile verification across breakpoints (768px, 480px)
- [ ] Touch-friendly button sizes (minimum 44px tap targets)
- [ ] Google Business Profile setup guide (PDF, for local businesses only)

**Lighthouse benchmarks from Top Dog (the standard to beat):**

| Metric | Desktop | Mobile |
|--------|---------|--------|
| Performance | 100 | 97 |
| Accessibility | 96 | 91 |
| Best Practices | 100 | 100 |
| SEO | 100 | 100 |

**Core Web Vitals targets (mobile):**

| Metric | Target |
|--------|--------|
| First Contentful Paint | < 1.5s |
| Largest Contentful Paint | < 2.5s |
| Total Blocking Time | < 50ms |
| Cumulative Layout Shift | < 0.1 |
| Speed Index | < 2.0s |

### Tier 3: Content Marketing (Weeks 2-4)

- [ ] Blog infrastructure: index page + individual article pages
- [ ] Article JSON-LD schema on each blog post
- [ ] Minimum 3 articles:
  - 1 educational ("What is [concept]?") — ~600 words
  - 1 comparison ("X vs Y: What's the Difference?") — ~700 words
  - 1 trend/benefit ("Why [audience] Are Doing [thing] in 2026") — ~650 words
- [ ] CTA box on each article driving to contact form
- [ ] All articles in sitemap
- [ ] Blog linked from nav and footer
- [ ] Local citations guide (PDF, for local businesses only): 9+ directory listings with copy-paste business description, NAP consistency rules

### Tier 4: Generative Engine Optimization / GEO (Ongoing)

This is the differentiator. This is what makes SimplWorks different from every other web design shop.

- [ ] **AI-pullable definition block**: A visible paragraph on the page containing every key fact about the business in one crawlable block. Company name, location, service description, product/service types, technology, cost model, founders, service area. This is the paragraph we want AI to extract and repeat.
- [ ] **FAQ optimization for AI extraction**: Every answer leads with a direct, quotable first sentence containing entity names and location. Add FAQ items that mirror AI queries: "What is [business]?", "Who is [business]?", "How does [product] work?", "What does [business] do?"
- [ ] **Entity-rich content**: Every section contains explicit entity relationships ("X does Y for Z in [location]")
- [ ] **Narrative control**: We write the answer we want AI systems to give. Not marketing copy — structured, factual, quotable statements.

**Validation (1-2 weeks post-launch):**
- Ask ChatGPT: "What is [business name]?" and "Tell me about [business name] in [city]"
- Ask Perplexity: Same queries (picks up new content faster)
- Check Google AI Overview for the business name
- Compare AI answers to the definition block. If it matches, GEO is working.

---

## Tech Stack Decision Tree

### When to use Next.js (deployed on Vercel)

Use Next.js when the site needs:
- Blog with dynamic routing (/blog/[slug])
- Server-side rendering or static generation
- Multiple pages with shared layout
- Image optimization (next/image is powerful)
- The client is on a Vercel-friendly plan

**Stack:** Next.js + React + CSS Modules or Tailwind + Vercel deployment
**Example:** Top Dog Vending

### When to use Static HTML (deployed on Cloudflare Workers)

Use static HTML when the site is:
- Single page with no blog (or blog can be added later)
- Simple lead capture form
- Client needs fastest possible turnaround
- No server-side logic needed

**Stack:** HTML + CSS + vanilla JS + Cloudflare Workers
**Example:** SimplWorks.ai, Higher Game Podcast

### Database / Backend

- **Lead capture:** Supabase. Direct REST API calls via fetch. No SDK needed for simple form submissions.
- **Table structure for leads:** name, email, phone, business, message, source (identifies which site the lead came from)
- **RLS policy:** Enable row-level security, create policy allowing inserts from anon role

### Analytics

- **Vercel sites:** `@vercel/analytics` package, add `<Analytics />` component to layout
- **Cloudflare sites:** Cloudflare Web Analytics (free, no JS needed if using Cloudflare)

---

## Page Structure Template

Every SimplWorks client site follows this section order (adjust based on business type):

1. **Navigation** — Logo, section links, CTA button. Fixed, 72px, blurred background.
2. **Hero** — Centered. Tag line, headline (with accent color emphasis), subtitle, primary + secondary CTA buttons.
3. **Services / What We Do** — 3-column grid (or 2-column for fewer items). Cards with icons.
4. **Pain Points / "Is This You?"** — 2-column grid of checkmark items. Only include if copy warrants it.
5. **Who We Serve** — 2-column grid with emoji icons. Identifies target audience.
6. **How It Works / Process** — 3-column grid of numbered step cards. Centered titles, left-aligned descriptions.
7. **About / Meet the Team** — Two-column: text left, highlight cards right. Bio focuses on business credibility, not coding background.
8. **FAQ** — Accordion-style cards. Centered within 780px container. Each item is a separate card.
9. **Contact / CTA** — Centered. Headline, subtitle, form, email + phone links, tagline.
10. **Footer** — Copyright, built-by credit.

Not every site needs every section. But this is the default order and any deviations should be intentional.

---

## Form Integration Standard

**CRITICAL SECURITY RULE: Never put API keys, Supabase URLs, or any credentials in client-side HTML or JavaScript. All database calls go through a server-side function. No exceptions.**

This was fixed on SimplWorks.ai on February 22, 2026 after the original build exposed the Supabase anon key in plain HTML. That mistake is now codified as a never-again rule.

### The Pattern: Client → Your Server → Supabase

The browser only talks to your own domain. Your server talks to Supabase. Credentials never touch the browser.

```
Browser → POST /api/contact (your domain) → Serverless function → Supabase REST API
```

### Front-End (HTML + JavaScript — NO credentials)

```html
<form id="strategy-form">
  <input type="text" id="lead-name" placeholder="Your name" required>
  <input type="email" id="lead-email" placeholder="Email" required>
  <input type="tel" id="lead-phone" placeholder="Phone (optional)">
  <input type="text" id="lead-business" placeholder="Business name (optional)">
  <textarea id="lead-message" rows="4" placeholder="Tell me about your project"></textarea>
  <button type="submit" id="submit-btn">Book a Strategy Call</button>
</form>
```

```javascript
// NO API keys. NO Supabase URLs. The form posts to YOUR OWN domain.
form.addEventListener('submit', async (e) => {
  e.preventDefault();
  // Disable button, show "Sending..."
  // Build payload: { name, email, phone, business, message }
  // POST to '/api/contact' (relative URL — hits your own server)
  // Headers: { 'Content-Type': 'application/json' }
  // Parse response JSON, check for success
  // Success: "Got it. I'll be in touch within 24 hours."
  // Error: "Something went wrong. Try again or email me directly."
  // Re-enable button
});
```

### Back-End: Cloudflare Workers (Static HTML Sites)

For static sites on Cloudflare Workers, the Worker script handles both static assets and API routes.

**Worker script (`src/index.js`):**

```javascript
export default {
  async fetch(request, env) {
    const url = new URL(request.url);

    // Handle form submissions server-side
    if (url.pathname === '/api/contact' && request.method === 'POST') {
      const body = await request.json();
      const payload = {
        name: body.name || null,
        email: body.email || null,
        phone: body.phone || null,
        business: body.business || null,
        message: body.message || null,
        source: 'your-site-name',
      };

      const res = await fetch(env.SUPABASE_URL + '/rest/v1/[table_name]', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          apikey: env.SUPABASE_KEY,
          Authorization: 'Bearer ' + env.SUPABASE_KEY,
          Prefer: 'return=minimal',
        },
        body: JSON.stringify(payload),
      });

      if (res.ok) {
        return new Response(JSON.stringify({ success: true }), {
          status: 200, headers: { 'Content-Type': 'application/json' },
        });
      }
      return new Response(JSON.stringify({ success: false }), {
        status: 500, headers: { 'Content-Type': 'application/json' },
      });
    }

    // Everything else: serve static assets
    return env.ASSETS.fetch(request);
  },
};
```

**Wrangler config (`wrangler.jsonc`):**

```jsonc
{
  "name": "your-worker-name",
  "main": "./src/index.js",
  "compatibility_date": "2026-02-06",
  "assets": {
    "directory": "./public",
    "binding": "ASSETS",
    "run_worker_first": ["/api/*"]
  }
}
```

**Setting secrets (credentials are encrypted, never in code):**

```bash
printf "https://[project-id].supabase.co" | CLOUDFLARE_API_TOKEN=[token] CLOUDFLARE_ACCOUNT_ID=[account-id] npx wrangler secret put SUPABASE_URL
printf "[anon-key]" | CLOUDFLARE_API_TOKEN=[token] CLOUDFLARE_ACCOUNT_ID=[account-id] npx wrangler secret put SUPABASE_KEY
```

### Back-End: Next.js API Routes (Vercel Sites)

For Next.js sites on Vercel, use API routes. Credentials come from Vercel environment variables (set in dashboard or CLI).

**API route (`app/api/leads/route.js`):**

```javascript
import { createClient } from '@supabase/supabase-js';

function getSupabase() {
  return createClient(
    process.env.SUPABASE_URL,       // NOT NEXT_PUBLIC_ prefix
    process.env.SUPABASE_ANON_KEY   // NOT NEXT_PUBLIC_ prefix
  );
}

export async function POST(request) {
  const body = await request.json();
  const supabase = getSupabase();

  const { error } = await supabase.from('[table_name]').insert([{
    name: body.name?.trim(),
    email: body.email?.trim() || null,
    phone: body.phone?.trim() || null,
    message: body.message?.trim() || null,
    source: 'your-site-name',
  }]);

  if (error) {
    return Response.json({ error: 'Something went wrong.' }, { status: 500 });
  }
  return Response.json({ success: true });
}
```

**IMPORTANT:** Use `process.env.SUPABASE_URL` — NOT `process.env.NEXT_PUBLIC_SUPABASE_URL`. The `NEXT_PUBLIC_` prefix exposes the variable to the browser. Server-only env vars stay server-only.

### Credential Storage Summary

| Platform | Where credentials live | How to set them |
|----------|----------------------|-----------------|
| **Cloudflare Workers** | Encrypted Worker secrets | `npx wrangler secret put VAR_NAME` |
| **Vercel (Next.js)** | Vercel environment variables | Vercel dashboard → Settings → Environment Variables, or `vercel env add` |

### The `source` Field

Every form submission includes a `source` field identifying which website the lead came from (e.g., `'simplworks-website'`, `'topdogvending'`). This is added server-side, not from the browser. It lets us track lead sources in one Supabase table.

### Security Checklist for Every Build

- [ ] **No API keys in HTML** — view-source the production site and search for "supabase", "apikey", "Bearer", "eyJ". Nothing should match.
- [ ] **No `NEXT_PUBLIC_` env vars for secrets** — only use `NEXT_PUBLIC_` for values that are safe to expose (like a site name). Never for API keys or URLs.
- [ ] **Form posts to your own domain** — the fetch URL should be `/api/contact` or similar, never an external Supabase URL.
- [ ] **Secrets are set on the hosting platform** — Cloudflare Worker secrets or Vercel env vars, not in code, not in `.env` files committed to git.
- [ ] **Test the form on production** — submit a test lead after deploy and verify it appears in Supabase.

---

## Client Handoff Deliverables

Every project delivery includes these documents:

| Document | Format | Contents |
|----------|--------|----------|
| SEO Optimization Report | PDF | Everything done in Tiers 1-4, Lighthouse scores, structured data details |
| Website Enhancement Report | PDF | Typography, layout, readability, accessibility improvements |
| Google Business Profile Guide | PDF | Step-by-step setup instructions (local businesses only) |
| Local Citations Guide | PDF | 9+ directory listings, copy-paste description, NAP rules, email migration if needed |
| Project Status Tracker | PDF | Complete checklist of what's done, what's pending, what needs client action |

**Generate as PDF.** Never HTML — email providers block .html attachments.

---

## Deployment Checklist

### Before going live:

- [ ] All Tier 1 SEO elements in place
- [ ] Form tested — submit a test lead, verify it appears in Supabase
- [ ] Mobile tested at 768px and 480px breakpoints
- [ ] All links working (nav, CTAs, email, phone)
- [ ] Favicon set
- [ ] OG image uploaded and tested (use opengraph.xyz to preview)
- [ ] Lighthouse mobile score: SEO 100, all others 90+
- [ ] Structured data validated (Google Rich Results Test)
- [ ] DNS configured (if custom domain ready)
- [ ] SSL active

### After going live:

- [ ] Verify site loads on custom domain
- [ ] Test form submission on production
- [ ] Submit sitemap to Google Search Console
- [ ] Set up analytics (Vercel Analytics or Cloudflare Web Analytics)
- [ ] Run Lighthouse on production URL (not localhost)
- [ ] AI citation test queries (1-2 weeks post-launch)
- [ ] Deliver client handoff documents

---

## Process Timeline Benchmarks

Based on Top Dog Vending (first implementation):

| Phase | Time |
|-------|------|
| Website build & deployment | ~4 hours |
| Tier 1: Technical SEO | ~1 hour |
| Tier 2: Performance + accessibility | ~2 hours |
| Tier 3: Blog + 3 articles + citations guide | ~3 hours |
| Tier 4: GEO (definition block, FAQ, entity optimization) | ~1 hour |
| Design polish (typography, layout, readability) | ~2 hours |
| Client documents (reports, guides, status tracker) | ~2 hours |
| **Total for a full digital launch** | **~15 hours across 2 days** |

These will tighten as the process is repeated.

---

## CSS Template

Every new project starts with these CSS variables (adjust accent color per brand):

```css
:root {
  --bg: #0a0a0a;
  --bg-alt: #111111;
  --bg-card: #161616;
  --border: rgba(255, 255, 255, 0.06);
  --border-hover: rgba(/* accent */, 0.4);
  --accent: /* brand color */;
  --accent-hover: /* darker brand color */;
  --accent-glow: rgba(/* accent */, 0.15);
  --text: #d1d5db;
  --text-dim: #9ca3af;
  --white: #f0f0f0;
}

body {
  font-family: 'Inter', sans-serif; /* or Montserrat for Next.js */
  background: var(--bg);
  color: var(--text);
  font-size: 18px;
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
}
```

---

## Prototype Reference: Top Dog Vending

**Client:** Emory & Ellie, Knoxville, TN
**Business:** AI-powered smart stores for apartment communities
**Built:** February 20-21, 2026
**Stack:** Next.js + React + Vercel + Supabase
**Live:** topdog-website-tau.vercel.app (pending domain: topdogvending.com)

**Results:**
- Desktop: Performance 100, Accessibility 96, Best Practices 100, SEO 100
- Mobile: Performance 97, Accessibility 91, Best Practices 100, SEO 100
- FCP: 1.2s, LCP: 2.0s, TBT: 10ms, CLS: 0, Speed Index: 1.9s

**What was delivered:**
- Full single-page website with blog (3 articles)
- 10-item FAQ with JSON-LD schema
- AI-pullable definition block
- Contact form connected to Supabase
- 5 client handoff documents (PDFs)
- Vercel Analytics installed

This is the benchmark. Every future build should match or exceed these numbers.

---

## What Makes This Different

Most web designers build a site and hand it over. SimplWorks delivers:

1. **A site that Google loves** (Tier 1-2: perfect Lighthouse scores, structured data, Core Web Vitals)
2. **A site that AI quotes** (Tier 4: GEO, definition blocks, FAQ optimization, narrative control)
3. **A site that converts** (Lead capture wired to real databases, conversion-focused layout, clear CTAs)
4. **A complete digital launch** (Website + SEO + GEO + blog + citations + client guides — one provider, everything handled)

The GEO layer is the competitive advantage. No one else is doing this at the small business level yet.

---

## Document History

| Date | Change |
|------|--------|
| Feb 22, 2026 | Created. Based on Top Dog Vending prototype (Feb 20-21, 2026). Placed in Cortex root for permanent reference. |
| Feb 22, 2026 | Added serverless function pattern for form security. No credentials in client-side code — all database calls go through server-side functions (Cloudflare Worker secrets or Vercel env vars). Added security checklist. |

---

*This is an internal Cortex reference document. It is not client-facing. Cortex reads this at the start of every new client website project. Update it as the process evolves and new patterns are established.*
