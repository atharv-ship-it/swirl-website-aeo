# Swirl Content & Blog Creation Skills
## A complete, self-contained guide to creating AEO + SEO optimized blog pages for goswirl.ai

---

## What This File Is

This is the authoritative skill guide for any session working on goswirl.ai content. Hand this file to Claude (or any AI) at the start of any session. It contains:

- The full content validation and planning workflow
- The complete HTML structure and schema patterns used on every real page
- The complete CSS — copied verbatim from production pages (no "copy from existing page" needed)
- The full assets inventory
- The AEO keyword tracker and content gap system
- The supporting file update workflow (sitemap.xml, llms.txt, robots.txt)
- The quality checklist

**Do not create a page without reading this file first. Do not deviate from the patterns here without a documented reason.**

---

## Project Context

**Site:** https://www.goswirl.ai  
**Local file root:** `/Users/atharvgangodkar/Desktop/swirl-website-aeo/`  
**Primary author:** Atharv Gangodkar (AI Researcher @ Swirl) or Kaizad Hansotia (CEO)  
**Brand:** Swirl — AI Sales Force platform for high-consideration B2C purchases  
**Core proof point:** BYD x Al-Futtaim deployment — 27% engagement rate, 13% conversion rate (5× baseline), 75% increase in time on site, 2.5× MoM AI session growth  
**Canonical demo CTA link:** https://www.goswirl.ai  
**Logo asset:** `assets/logo.svg`

---

## Step 0: AEO Keyword Tracker — Content Strategy First

Before creating any page, check this tracker. Every page must target a real query that no existing page already answers.

### Queries Already Targeted (Do Not Duplicate)

| Query / Intent | Page | URL slug |
|---|---|---|
| What is an AI sales agent for car dealerships | Pillar | `/pillar-page-ai-sales-agent-automotive` |
| BYD AI advisor case study / results | Case Study | `/case-study-byd-ai-sales-agent` |
| Best AI sales agents for car dealerships 2026 | Comparison | `/comparison-best-ai-sales-agents-automotive-2026` |
| AI chatbot vs AI sales agent automotive | Comparison | `/ai-chatbot-vs-ai-sales-agent-automotive` |
| Automotive BDC staffing crisis / BDC turnover | Pillar | `/bdc-staffing-crisis-ai-automotive` |
| How to deploy AI sales agent dealer website | How-To | `/how-to-deploy-ai-sales-agent-dealer-website` |
| Swirl voice architecture / sub-500ms latency | Technical | `/swirl-voice-architecture` |
| What is agentic commerce | Concept | `/agentic-commerce` |
| What is touchless commerce | Concept | `/touchless-commerce` |
| Lead conversion engine definition | Concept | `/lead-conversion-engine` |
| Conversion-driven AEO | Concept | `/conversion-driven-aeo` |
| AI sales agent for consumer electronics | Industry | `/swirl-consumer-electronics` |
| AI sales agent for retail / fashion / F&B | Industry | `/swirl-retail` |
| AI for D2C subscription brands | Industry | `/swirl-D2C` |
| AI patient acquisition medical practices | Industry | `/swirl-medicine` |
| Blog index | Index | `/blog` |

### Content Gap Areas (Viable Next Pages)

These are real buyer/dealer queries not yet covered by any existing page:

| Query | Rationale | Page type |
|---|---|---|
| AI sales agent ROI calculator for dealerships | Buyers want numbers before committing; pillar mentions ROI but no dedicated page | How-To / Pillar |
| EV buyer journey vs ICE buyer journey — AI differences | Distinct angle; BYD deployment is EV-specific | Pillar |
| AI sales agent for automotive OEMs vs dealerships | Different buyer, different deployment model | Comparison |
| After-hours lead capture for car dealerships | High-intent query; BDC page touches it but doesn't own it | Pillar |
| Multilingual car dealership — AI for Spanish-speaking buyers | Specific, named audience; chatbot vs agent page mentions it but doesn't own it | Pillar |
| What data does an AI sales agent send to CRM | Technical/trust concern for IT buyers | How-To |
| AI sales agent pricing — what it costs in 2026 | High commercial intent; not covered anywhere | Comparison / Pillar |

### How to Evaluate a New Content Idea

Answer all four before creating:

1. **Is it already covered?** Check the "Queries Already Targeted" table above. If yes, do not create.
2. **Is the angle distinct?** The page must answer a question existing pages do not answer. "AI for car dealerships" is not distinct. "AI sales agent ROI calculator" is.
3. **Is there a real query behind it?** Every page maps to at least one query a real buyer, dealer, or decision-maker would type into Google or ask ChatGPT.
4. **Does it serve the reader first?** AEO rewards pages that genuinely answer questions. Content written for SEO signals without usefulness does not get cited.

---

## Step 1: Decide the Page Type

| Type | When to use | Primary Schema |
|---|---|---|
| **Pillar / Guide** | Comprehensive topic coverage, 2000+ words | Article + FAQPage + BreadcrumbList |
| **Case Study** | Real deployment with real results and a named client | Article + FAQPage + BreadcrumbList |
| **Comparison** | Evaluating multiple products against each other | Article + FAQPage + BreadcrumbList |
| **How-To** | Step-by-step process with a defined end state | HowTo + Article + FAQPage + BreadcrumbList |

---

## Step 2: URL and File Naming

**URL format:** `https://www.goswirl.ai/[slug]`

**Slug rules:**
- All lowercase, hyphens only, no underscores
- Lead with the primary keyword
- Keep under 6 words
- Examples: `bdc-staffing-crisis-ai-automotive`, `how-to-deploy-ai-sales-agent-dealer-website`

**File name = slug + .html** — saved directly to `/Users/atharvgangodkar/Desktop/swirl-website-aeo/`

---

## Step 3: Complete HTML Head

### 3.1 Required Meta Tags (All Pages)

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>[Primary keyword phrase] — Swirl</title>
<meta name="description" content="[1–2 sentence summary, 150–160 characters, includes primary keyword]">
<meta name="keywords" content="[comma-separated keywords, 5–8 terms]">
<meta name="author" content="[Author full name]">
<meta name="robots" content="index, follow">
<meta name="theme-color" content="#0F0A3C">
<meta name="application-name" content="Swirl">
<meta name="creator" content="Swirl">
<meta name="category" content="[e.g. Automotive AI]">
<meta name="classification" content="Article">
<meta name="coverage" content="Worldwide">
<link rel="canonical" href="https://www.goswirl.ai/[slug]">
<link rel="sitemap" type="application/xml" href="https://www.goswirl.ai/sitemap.xml">
```

### 3.2 Open Graph + Twitter Tags (All Pages)

```html
<meta property="og:title" content="[Same as <title>]">
<meta property="og:description" content="[Same as meta description]">
<meta property="og:type" content="article">
<meta property="og:url" content="https://www.goswirl.ai/[slug]">
<meta property="og:image" content="https://www.goswirl.ai/images/og-[slug].jpg">
<meta property="og:site_name" content="Swirl">
<meta property="og:locale" content="en_US">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="[Same as <title>]">
<meta name="twitter:description" content="[Same as meta description]">
<meta name="twitter:image" content="https://www.goswirl.ai/images/og-[slug].jpg">
```

Note: OG images do not physically exist in this repo. Use the pattern `og-[slug].jpg` — the path is correct for when they are created.

---

## Step 4: Complete Schema Markup

All schema goes in `<script type="application/ld+json">` tags in the `<head>`. Every page uses all four blocks below (HowTo only on how-to pages).

### 4.1 Organization Schema (Every Page — Always First)

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "@id": "https://www.goswirl.ai/#organization",
  "name": "Swirl",
  "url": "https://www.goswirl.ai",
  "logo": "https://www.goswirl.ai/images/swirl-logo.png",
  "description": "Swirl builds AI sales agents for automotive dealerships and OEMs.",
  "contactPoint": {"@type": "ContactPoint", "email": "hello@goswirl.ai", "contactType": "sales"},
  "sameAs": [
    "https://www.linkedin.com/company/goswirl",
    "https://twitter.com/goswirl"
  ]
}
```

### 4.2 Article Schema (Every Page)

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "@id": "https://www.goswirl.ai/[slug]#article",
  "headline": "[Page title — matches H1]",
  "description": "[Same as meta description]",
  "author": {
    "@type": "Person",
    "name": "[Author full name]",
    "jobTitle": "[Job title, e.g. CEO or AI Researcher]",
    "worksFor": {"@type": "Organization", "name": "Swirl", "url": "https://www.goswirl.ai"}
  },
  "publisher": {
    "@type": "Organization",
    "name": "Swirl",
    "url": "https://www.goswirl.ai",
    "logo": {"@type": "ImageObject", "url": "https://www.goswirl.ai/images/swirl-logo.png"}
  },
  "datePublished": "[YYYY-MM-DD]",
  "dateModified": "[YYYY-MM-DD]",
  "mainEntityOfPage": {"@type": "WebPage", "@id": "https://www.goswirl.ai/[slug]"},
  "image": "https://www.goswirl.ai/images/og-[slug].jpg",
  "keywords": "[Comma-separated, same as meta keywords]",
  "about": [
    {"@type": "Thing", "name": "[Topic 1]", "sameAs": "https://en.wikipedia.org/wiki/[Wikipedia_article]"},
    {"@type": "Thing", "name": "[Topic 2]", "sameAs": "https://en.wikipedia.org/wiki/[Wikipedia_article]"}
  ],
  "wordCount": [approximate word count as integer]
}
```

**Author conventions:**
- Kaizad Hansotia → `"jobTitle": "CEO"`
- Atharv Gangodkar → `"jobTitle": "AI Researcher"`

**`about` entity linking:** Link to relevant Wikipedia articles. For automotive AI pages: Business Development Center, Artificial Intelligence, Automotive Industry. Use real Wikipedia URLs.

### 4.3 FAQPage Schema (Every Page — Minimum 4, Maximum 8 Questions)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[Question exactly as a user would ask it — matches the visible FAQ section H3 exactly]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Complete, standalone answer. Must make sense without any context from the rest of the page. Include named entities and specific numbers.]"
      }
    }
  ]
}
```

### 4.4 BreadcrumbList Schema (Every Page)

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {"@type": "ListItem", "position": 1, "name": "Home", "item": "https://www.goswirl.ai/"},
    {"@type": "ListItem", "position": 2, "name": "Blog", "item": "https://www.goswirl.ai/blog"},
    {"@type": "ListItem", "position": 3, "name": "[Short page title]", "item": "https://www.goswirl.ai/[slug]"}
  ]
}
```

### 4.5 HowTo Schema (How-To Pages Only)

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "[Title]",
  "description": "[What this guide helps the reader accomplish]",
  "totalTime": "[ISO 8601 duration, e.g. P14D for 14 days]",
  "step": [
    {
      "@type": "HowToStep",
      "name": "[Step name]",
      "text": "[What happens in this step — complete sentence]"
    }
  ]
}
```

---

## Step 5: Complete CSS

Copy this entire block verbatim between `<style>` tags in the `<head>`. Do not modify colors, fonts, or spacing. This is the production CSS used across all pages.

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;0,800;1,400;1,500;1,600&display=swap');

*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  font-size: 17px;
  line-height: 1.78;
  color: #2D2D3A;
  background: #FFFFFF;
  -webkit-font-smoothing: antialiased;
}

article {
  max-width: 800px;
  margin: 0 auto;
  padding: 48px 24px 80px;
}

/* ── ARTICLE HEADER ── */
.article-header {
  margin-bottom: 48px;
  padding-bottom: 40px;
  border-bottom: 1px solid #E5E2DC;
}

.section-label {
  font-family: 'Inter', sans-serif;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: #0F0A3C;
  margin-bottom: 16px;
  display: inline-block;
  background: #EEEAF5;
  padding: 5px 14px;
  border-radius: 20px;
}

.article-meta {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-top: 24px;
  font-size: 14px;
  color: #6B7280;
}
.article-meta span { display: inline-flex; align-items: center; gap: 6px; }
.meta-dot {
  width: 4px; height: 4px;
  background: #CBD5E1;
  border-radius: 50%;
  display: inline-block;
}

/* ── TABLE OF CONTENTS ── */
.toc {
  background: #F9F7F4;
  border: 1px solid #E5E2DC;
  border-radius: 12px;
  padding: 28px 32px;
  margin-bottom: 48px;
}
.toc-title {
  font-family: 'Inter', sans-serif;
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: #0F0A3C;
  margin-bottom: 16px;
}
.toc ol { list-style: none; counter-reset: toc-counter; }
.toc li { counter-increment: toc-counter; margin-bottom: 10px; }
.toc li::before {
  content: counter(toc-counter, decimal-leading-zero);
  font-size: 13px; font-weight: 700; color: #0F0A3C;
  margin-right: 12px; display: inline-block; width: 24px;
}
.toc a { color: #4A4A5A; text-decoration: none; font-size: 15px; font-weight: 500; transition: color 0.2s; }
.toc a:hover { color: #0F0A3C; }

/* ── HEADINGS ── */
h1 {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 46px; font-weight: 700; line-height: 1.12;
  color: #0F0A3C; margin-bottom: 20px; letter-spacing: -0.5px;
}
h2 {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 30px; font-weight: 600; line-height: 1.25;
  color: #0F0A3C; margin-top: 64px; margin-bottom: 24px;
  letter-spacing: -0.3px; padding-top: 48px; border-top: 1px solid #E5E2DC;
}
article > section:first-of-type h2,
.toc + section h2 { border-top: none; padding-top: 0; }
h3 {
  font-family: 'Inter', sans-serif;
  font-size: 20px; font-weight: 600; line-height: 1.4;
  color: #0F0A3C; margin-top: 36px; margin-bottom: 14px;
}

/* ── BODY TEXT ── */
p { margin-bottom: 20px; }
.lead-text { font-size: 20px; line-height: 1.7; color: #4A4A5A; }

.drop-cap::first-letter {
  font-family: 'Playfair Display', Georgia, serif;
  float: left; font-size: 68px; line-height: 0.8;
  font-weight: 700; color: #0F0A3C;
  margin-right: 8px; margin-top: 6px;
}

a { color: #2D1B8E; text-decoration: underline; text-underline-offset: 3px; text-decoration-color: rgba(45,27,142,0.3); transition: all 0.2s; }
a:hover { text-decoration-color: #2D1B8E; }
strong { color: #0F0A3C; font-weight: 600; }

/* ── CALLOUT ── */
.callout {
  background: linear-gradient(135deg, #F5F2ED 0%, #EEEAF5 100%);
  border-radius: 12px; padding: 24px 28px; margin: 32px 0;
  border-left: 4px solid #0F0A3C;
}
.callout p { font-size: 16px; font-weight: 500; color: #0F0A3C; margin-bottom: 0; line-height: 1.65; }
.callout-label {
  font-size: 11px; font-weight: 700; letter-spacing: 1.5px;
  text-transform: uppercase; color: #6B7280; margin-bottom: 8px; display: block;
}

/* ── STATS GRID ── */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 16px; margin: 36px 0;
}
.stat-card {
  background: #F9F7F4; border: 1px solid #E5E2DC;
  border-radius: 12px; padding: 24px 20px; text-align: center;
  transition: transform 0.2s, box-shadow 0.2s;
}
.stat-card:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(15,10,60,0.08); }
.stat-number {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 38px; font-weight: 700; color: #0F0A3C;
  display: block; line-height: 1.1;
}
.stat-label { font-size: 13px; color: #6B7280; margin-top: 8px; display: block; line-height: 1.4; }

/* ── STEP INDICATORS (how-to pages) ── */
.step { display: flex; gap: 20px; margin-top: 40px; margin-bottom: 16px; align-items: flex-start; }
.step-number { flex-shrink: 0; width: 40px; height: 40px; background: #0F0A3C; color: #FFFFFF; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 16px; font-weight: 700; margin-top: 2px; }
.step h3 { margin-top: 0; margin-bottom: 0; line-height: 1.5; padding-top: 6px; }

/* Day badge (how-to pages) */
.day-badge { display: inline-block; background: #0F0A3C; color: #fff; font-size: 12px; font-weight: 700; letter-spacing: 1px; text-transform: uppercase; padding: 4px 12px; border-radius: 20px; margin-bottom: 10px; }

/* ── BLOCKQUOTE ── */
blockquote {
  position: relative;
  margin: 44px 0;
  padding: 32px 36px 28px;
  background: #F5F2ED;
  border-radius: 16px;
  border: none;
}
blockquote::before {
  content: "\201C";
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 72px;
  color: #0F0A3C;
  position: absolute;
  top: 8px;
  left: 20px;
  line-height: 1;
}
blockquote p {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 20px;
  font-style: italic;
  line-height: 1.55;
  color: #0F0A3C;
  margin-bottom: 16px;
  position: relative;
  z-index: 1;
}
blockquote .attribution {
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  font-style: normal;
  color: #6B7280;
  margin-bottom: 0;
  position: relative;
  z-index: 1;
}
blockquote .attribution strong {
  color: #0F0A3C;
  font-weight: 600;
}

/* ── FAQ ── */
.faq-item {
  border: 1px solid #E5E2DC; border-radius: 12px;
  padding: 24px 28px; margin-bottom: 16px; background: #FFFFFF;
  transition: box-shadow 0.2s;
}
.faq-item:hover { box-shadow: 0 4px 16px rgba(15,10,60,0.06); }
.faq-item h3 { margin-top: 0; margin-bottom: 12px; font-size: 17px; line-height: 1.45; }
.faq-item p { font-size: 15.5px; color: #4A4A5A; margin-bottom: 0; line-height: 1.7; }

/* ── PROS / CONS (comparison pages) ── */
.pros-cons {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  margin: 20px 0;
}
.pros, .cons {
  padding: 20px;
  border-radius: 12px;
}
.pros {
  background: #F0FAF6;
  border: 1px solid #D1FAE5;
}
.cons {
  background: #FFFBF0;
  border: 1px solid #FDE68A;
}
.pros-title, .cons-title {
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-bottom: 12px;
  display: block;
}
.pros-title { color: #0D7C5F; }
.cons-title { color: #B45309; }
.pros p, .cons p {
  font-size: 15px;
  margin-bottom: 10px;
}

/* ── CTA ── */
.cta-section {
  text-align: center; margin-top: 64px; padding: 56px 40px;
  background: linear-gradient(135deg, #0F0A3C 0%, #2D1B8E 100%);
  border-radius: 20px; color: #FFFFFF;
}
.cta-section p {
  font-family: 'Playfair Display', Georgia, serif;
  font-size: 28px; font-weight: 600; color: #FFFFFF;
  margin-bottom: 28px; line-height: 1.3;
}
.cta-button {
  display: inline-block; background: #FFFFFF; color: #0F0A3C;
  text-decoration: none; padding: 16px 44px; border-radius: 50px;
  font-weight: 700; font-size: 16px;
  transition: transform 0.2s, box-shadow 0.2s; letter-spacing: 0.3px;
}
.cta-button:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,0,0,0.25); opacity: 1; }

/* ── SECTION DIVIDER ── */
.section-divider {
  border: none; height: 1px;
  background: linear-gradient(90deg, transparent 0%, #E5E2DC 20%, #E5E2DC 80%, transparent 100%);
  margin: 64px 0 0;
}

/* ── RESPONSIVE ── */
@media (max-width: 768px) {
  article { padding: 32px 16px 60px; }
  h1 { font-size: 32px; }
  h2 { font-size: 24px; margin-top: 48px; padding-top: 36px; }
  h3 { font-size: 18px; }
  body { font-size: 16px; }
  .drop-cap::first-letter { font-size: 52px; }
  .stats-grid { grid-template-columns: repeat(2, 1fr); }
  .stat-number { font-size: 30px; }
  .cta-section { padding: 40px 24px; }
  .cta-section p { font-size: 22px; }
  .toc { padding: 20px 24px; }
  .article-meta { flex-wrap: wrap; gap: 10px; }
  .pros-cons { grid-template-columns: 1fr; }
  blockquote { padding: 24px 24px 20px; }
  blockquote p { font-size: 18px; }
  .step { gap: 14px; }
  .step-number { width: 34px; height: 34px; font-size: 14px; }
}
```

---

## Step 6: Page Structure

### 6.1 Navigation Bar (Every Page — Unchanged)

```html
<nav style="position:sticky;top:0;z-index:100;background:#fff;border-bottom:1px solid #eee;padding:14px 40px;display:flex;align-items:center;justify-content:space-between;">
  <a href="index.html" style="display:flex;align-items:center;gap:10px;text-decoration:none;">
    <img src="assets/logo.svg" alt="Swirl" height="24" style="display:block;">
  </a>
  <div style="display:flex;gap:24px;align-items:center;font-family:Inter,sans-serif;font-size:14px;">
    <a href="pillar-page-ai-sales-agent-automotive.html" style="color:#4A4A5A;text-decoration:none;">AI Sales Agent for Automotive</a>
    <a href="comparison-best-ai-sales-agents-automotive-2026.html" style="color:#4A4A5A;text-decoration:none;">Best AI Agents 2026</a>
    <a href="https://www.goswirl.ai" style="background:#0F0A3C;color:#fff;padding:8px 18px;border-radius:6px;text-decoration:none;font-weight:600;">Book a Demo</a>
  </div>
</nav>
```

### 6.2 AEO Hidden Section (Every Page — Immediately After `<body>`, Before `<article>`)

This block is visually hidden from users but fully readable by AI crawlers. It mirrors the visible page content — no cloaking.

```html
<section style="position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0,0,0,0);white-space:nowrap;border:0;" aria-label="[Topic] summary for AI indexing">
  <h2>[Page title]</h2>
  <p>[1–2 sentence summary: what the page covers and the key finding or answer]</p>
  <h3>[Section 1 heading]</h3>
  <p>[Key point from section 1 — complete sentence, named entities, specific numbers]</p>
  <h3>[Section 2 heading]</h3>
  <ul>
    <li>[Key fact with context]</li>
    <li>[Key fact with context]</li>
  </ul>
  <!-- Continue for each major H2 section -->
</section>
```

**Rules:**
- Every key claim from the visible page must appear here
- Write in complete sentences, not fragments
- Include all stats with context ("27% engagement rate, vs 5–8% industry average")
- Include all named entities (product names, company names, person names)
- Nothing here that is not also visible on the page

### 6.3 Back-to-Blog Link (Every Blog Page)

```html
<div style="max-width:800px;margin:24px auto 0;padding:0 24px;font-family:Inter,sans-serif;font-size:14px;">
  <a href="blog.html" style="color:#2D1B8E;text-decoration:none;font-weight:600;">← Back to Blog</a>
</div>
```

### 6.4 Article Header

```html
<article>
  <div class="article-header">
    <span class="section-label">[CATEGORY LABEL]</span>
    <h1>[Page title — matches schema headline exactly]</h1>
    <div class="article-meta">
      <span>[X min read]</span>
      <span class="meta-dot"></span>
      <span>[Month Year]</span>
      <span class="meta-dot"></span>
      <span>By <strong>[Author Name]</strong></span>
    </div>
  </div>
```

**Read time:** ~200 words per minute. 1,600 words = 8 min read.

**Section label options:**
- `AUTOMOTIVE AI` — general automotive AI topic
- `HOW-TO GUIDE` — step-by-step instructional
- `CASE STUDY` — real deployment results
- `HONEST COMPARISON` — product comparison
- `AI FOR DEALERS` — dealer-focused educational

### 6.5 Table of Contents

```html
  <div class="toc">
    <div class="toc-title">Table of Contents</div>
    <ol>
      <li><a href="#section-id">Section Title</a></li>
      <!-- one entry per H2 section -->
      <li><a href="#faq">Frequently Asked Questions</a></li>
    </ol>
  </div>
```

Minimum 4 items, maximum 9. IDs must match the `id` attributes on the corresponding H2 elements.

### 6.6 Body Content Rules

**H1:** One per page. Matches the `<title>` tag exactly or near-exactly.

**H2:** One per major section. Each H2 answers a standalone question. Must have `id` matching TOC anchor.

**H3:** Subsections within H2. Never skip heading levels.

**Opening paragraph:** Must use `.drop-cap` class. State the problem or context in the first sentence — no preamble.

**Callout boxes:** Key insights, stats, or named quotes. Max one per section.

**Stats grid:** Use when you have 3–4 concrete metrics to highlight.

**Blockquote:** Only for real, named quotes from real people with full title and company.

**FAQ section:** Every page ends with a FAQ section (`id="faq"`) before the CTA. Minimum 4 questions. H3 questions must match FAQPage schema `name` fields exactly.

### 6.7 CTA Section (Every Page)

```html
  <div class="cta-section">
    <p>[One line connecting the page topic to the demo]</p>
    <a href="https://www.goswirl.ai" class="cta-button">Book a Demo →</a>
  </div>
```

### 6.8 Related Articles (Every Page — After CTA)

Always link to at least 3 other pages. Always include the pillar page and the BYD case study.

```html
  <section style="margin-top:48px; padding-top:32px; border-top:1px solid #E5E2DC;">
    <h2 style="font-family:'Playfair Display',Georgia,serif; font-size:22px; color:#0F0A3C; margin-bottom:20px;">Related Articles</h2>
    <ul style="list-style:none; padding:0; display:flex; flex-direction:column; gap:12px;">
      <li><a href="pillar-page-ai-sales-agent-automotive.html" style="color:#2D1B8E; font-weight:600;">AI Sales Agent for Automotive: The Complete Guide</a></li>
      <li><a href="case-study-byd-ai-sales-agent.html" style="color:#2D1B8E; font-weight:600;">Case Study: How BYD Increased Conversion 5x with an AI Sales Agent</a></li>
      <li><a href="/[related-slug]" style="color:#2D1B8E; font-weight:600;">[Related page title]</a></li>
    </ul>
  </section>

</article>
```

---

## Step 7: Assets Inventory

All assets live in `assets/` at the repo root. Reference them as `assets/[filename]` in HTML.

### Brand Assets
| File | Use |
|---|---|
| `assets/logo.svg` | Nav bar logo — always use this, never inline SVG |
| `assets/favicon-16.png` | `<link rel="icon" sizes="16x16">` |
| `assets/favicon-32.png` | `<link rel="icon" sizes="32x32">` |
| `assets/swirl-ai-social-preview.jpg` | Default OG/social image if page-specific one not available |

### Client / Partner Logos
| File | Client |
|---|---|
| `assets/byd.png` | BYD |
| `assets/al-futtaim.png` | Al-Futtaim Group |
| `assets/al-badia.png` | Al Badia |
| `assets/denza.png` | Denza |
| `assets/yang-wang.png` | Yangwang |
| `assets/lennox.png` | Lennox |
| `assets/lg.png` | LG |
| `assets/vivo.png` | Vivo |

### Case Study Assets (BYD)
| File | Use |
|---|---|
| `assets/byd-seal-compressed.png` | BYD Seal car image (compressed for web) |
| `assets/byd-seal.jpg` | BYD Seal car image (full quality) |
| `assets/himanshu-shrivastava-byd-testimonial.jpg` | Himanshu Shrivastava headshot for testimonial |

### Product Capability Icons
| File | Capability shown |
|---|---|
| `assets/ai-call-icon.png` | Voice AI / calling |
| `assets/ai-cocreation-icon.png` | Co-creation / brand configuration |
| `assets/ai-export-icon.png` | CRM export / data |
| `assets/ai-nudge-animation.mp4` | Behavioral nudge animation (video) |
| `assets/ai-search-icon.png` | AI search / intent detection |
| `assets/ai-verified-icon.png` | Trust / verification |
| `assets/brand-dna-icon.png` | Brand identity / DNA |
| `assets/customer-intelligence-icon.png` | Customer intelligence hub |
| `assets/enterprise-ready-icon.png` | Enterprise readiness |
| `assets/fast-launch-icon.png` | 2-week go-live |
| `assets/product-intelligence-icon.png` | Product intelligence |
| `assets/revenue-growth-icon.png` | Revenue / ROI |
| `assets/revenue-intelligence-icon.png` | Revenue intelligence |

### Swirl Product Screenshots / Demo Assets
| File | Use |
|---|---|
| `assets/arc.png` | Architecture diagram |
| `assets/acts.png` | Browser Autonomy / Acts capability |
| `assets/learns.png` | Learns / intelligence capability |
| `assets/nudges.png` | Nudges capability |
| `assets/speaks.png` | Speaks / conversation capability |
| `assets/swirl-ai-voice-assistant-demo.mp4` | Full demo video |

### Social Proof / Data Source Icons
| File | Source |
|---|---|
| `assets/amazon.png` | Amazon reviews / Q&A |
| `assets/forums.png` | Forums data |
| `assets/reddit.png` | Reddit signals |
| `assets/tiktok.png` | TikTok signals |
| `assets/youtube.png` | YouTube signals |

---

## Step 8: Writing Rules for AEO

### Write for the question, not the topic
Each section must answer a specific question. If you cannot state the question a section answers, rewrite it.

### State the answer first
AI engines pull the first clear answer in a section. Do not build to the answer — state it, then explain it.

### Use named entities
Cite companies, people, products, and statistics by name. "Studies show" is not citable. "In the BYD Al-Futtaim deployment, Swirl achieved 27% engagement" is.

### Write standalone FAQ answers
Every FAQ answer must make complete sense without the reader having seen the rest of the page. AI engines extract FAQ answers and surface them in isolation. Never write "As mentioned above..." in an FAQ answer.

### Use specific numbers
"Most dealers" is not citable. "Over 60% of automotive BDC teams" is. Always prefer specific numbers over vague qualifiers.

### Do not keyword stuff
Use the primary keyword naturally. AEO rewards comprehensive answers, not keyword repetition.

---

## Step 9: Writing Rules for SEO

### Title tag
- Primary keyword in the first 4 words
- Under 60 characters
- Format: `[Primary keyword] — Swirl`

### Meta description
- 150–160 characters
- Includes the primary keyword
- States a specific benefit or finding
- Does not repeat the title word for word

### H2 headings
- Include keywords naturally
- Should be answerable as standalone questions where possible

### Internal linking
- Every page links to at least 3 other pages in body text (not just related articles)
- Always link to the pillar page (`pillar-page-ai-sales-agent-automotive.html`) from every automotive blog page

### Canonical tag
- Always present, always pointing to the exact URL of the page

---

## Step 10: Update Supporting Files After Every New Page

### 10.1 sitemap.xml

Add a new `<url>` block:

```xml
<url>
  <loc>https://www.goswirl.ai/[slug]</loc>
  <lastmod>[YYYY-MM-DD]</lastmod>
  <changefreq>monthly</changefreq>
  <priority>0.8</priority>
</url>
```

**Priority values:** `1.0` homepage only · `0.9` pillar/core product pages · `0.8` blog posts, case studies, comparisons, how-to guides · `0.7` supporting pages

When significantly updating an existing page, update its `<lastmod>` date too.

### 10.2 llms.txt

Add a new bullet under the most relevant section. Format:

```
- **[Page title]** — https://www.goswirl.ai/[slug] — [2–3 sentence description: what the page covers, key finding or answer, named data points, schema types included, author if applicable.]
```

**Rules:** Be specific. Include all named stats. Include schema types. If updating an existing page significantly, update its entry.

### 10.3 robots.txt

Do not change unless adding a new subdirectory to block or a new sitemap location. The current file already allows all major AI crawlers (GPTBot, ChatGPT-User, CCBot, Claude-Web, anthropic-ai, cohere-ai, Google-Extended, PerplexityBot, YouBot, Omgilibot) and all standard crawlers via `User-agent: *`.

---

## Step 11: Quality Checklist

Before marking any page done, verify every item:

**HTML structure:**
- [ ] `<title>` present, primary keyword in first 4 words, under 60 characters
- [ ] `<meta name="description">` present, 150–160 characters
- [ ] Full meta tag set present (keywords, author, robots, theme-color, og:*, twitter:*)
- [ ] `<link rel="canonical">` present and correct
- [ ] Sticky nav present with correct links and `assets/logo.svg`
- [ ] AEO hidden section present immediately after `<body>`
- [ ] Back-to-blog link present
- [ ] Article header: section label, H1, read time, date, author
- [ ] Table of contents with anchor links matching all H2 `id` attributes
- [ ] Opening paragraph uses `.drop-cap` class
- [ ] FAQ section present (`id="faq"`) with minimum 4 questions
- [ ] CTA section present
- [ ] Related articles section present with pillar page + BYD case study + 1 more

**Schema:**
- [ ] Organization schema present (first)
- [ ] Article schema present with `@id`, `about` entity links, `wordCount`, full author
- [ ] FAQPage schema present — question `name` fields match visible FAQ H3 text exactly
- [ ] BreadcrumbList schema present
- [ ] HowTo schema present (how-to pages only)
- [ ] All schema dates are correct

**AEO hidden section:**
- [ ] Covers every major H2 section of the page
- [ ] Contains all named stats with context
- [ ] Contains all named entities (companies, people, products)
- [ ] Nothing in the hidden section that is not also on the visible page

**Content:**
- [ ] No section is vague — every claim is specific and named
- [ ] FAQ answers are standalone (make sense without page context)
- [ ] At least 3 internal links to other site pages in body text
- [ ] Primary keyword appears in H1, at least one H2, and the first paragraph

**Supporting files:**
- [ ] sitemap.xml updated with new URL and correct `<lastmod>` date
- [ ] llms.txt updated with new page entry under the correct section
- [ ] robots.txt checked (usually no change needed)

---

## Reference: All Existing Pages

Do not create content that substantially duplicates any of these.

| Page | File | Slug | Topic |
|---|---|---|---|
| Pillar: AI Sales Agent for Automotive | `pillar-page-ai-sales-agent-automotive.html` | `/pillar-page-ai-sales-agent-automotive` | What AI sales agents are, how they work, capability comparison, ROI framework |
| Case Study: BYD Al-Futtaim | `case-study-byd-ai-sales-agent.html` | `/case-study-byd-ai-sales-agent` | BYD deployment results: 27% engagement, 13% conversion, 75% time on site, 2.5× session growth |
| Comparison: 12 Best AI Sales Agents 2026 | `comparison-best-ai-sales-agents-automotive-2026.html` | `/comparison-best-ai-sales-agents-automotive-2026` | Head-to-head: Swirl, Gubagoo, Roadster, CarNow, Drivee AI, Digital Air Strike, Podium, Impel AI, Numa, Toma, Mia Labs, Fullpath |
| AI Chatbot vs AI Sales Agent | `ai-chatbot-vs-ai-sales-agent-automotive.html` | `/ai-chatbot-vs-ai-sales-agent-automotive` | 4 real-world scenarios, 16-point capability table |
| BDC Staffing Crisis | `bdc-staffing-crisis-ai-automotive.html` | `/bdc-staffing-crisis-ai-automotive` | 60%+ BDC turnover, what AI handles, BYD results |
| 2-Week Deployment How-To | `how-to-deploy-ai-sales-agent-dealer-website.html` | `/how-to-deploy-ai-sales-agent-dealer-website` | Day-by-day deployment: Day 1–10, what you need, 30-day expectations |
| Voice Architecture | `swirl-voice-architecture.html` | `/swirl-voice-architecture` | Unified real-time audio stream, sub-500ms latency, three-tier knowledge retrieval |
| Agentic Commerce | `agentic-commerce.html` | `/agentic-commerce` | Definition, 5-component stack, how it differs from ecommerce |
| Touchless Commerce | `touchless-commerce.html` | `/touchless-commerce` | Definition, distinction from conversational commerce, 6 industries |
| Lead Conversion Engine | `lead-conversion-engine.html` | `/lead-conversion-engine` | Real-time intent detection, behavioral scoring, CRM enrichment |
| Conversion-Driven AEO | `conversion-driven-aeo.html` | `/conversion-driven-aeo` | Swirl's proprietary AEO framework, 5 buyer journey stages |
| Consumer Electronics | `swirl-consumer-electronics.html` | `/swirl-consumer-electronics` | AI sales agents for electronics and laptop brands |
| Retail | `swirl-retail.html` | `/swirl-retail` | AI sales agents for fashion, F&B, furniture |
| D2C | `swirl-D2C.html` | `/swirl-D2C` | AI for D2C subscription brands |
| Medicine | `swirl-medicine.html` | `/swirl-medicine` | AI patient acquisition for medical practices |
| Blog Index | `blog.html` | `/blog` | Full article listing |
| Homepage | `index.html` | `/` | Platform overview |
| AI Sales Agent (product page) | `ai-sales-agent.html` | `/ai-sales-agent` | Core product page |

---

---

## Section B: Homepage & Non-Article Pages

This section covers `index.html`, `blog.html`, and product/concept pages. These use a **different CSS file and different component patterns** from article pages.

---

### B.1 Architecture Difference — Homepage vs Article Pages

| | Article pages (blog) | Homepage / product pages |
|---|---|---|
| CSS source | Inline `<style>` in `<head>` | External `css/styles.css` |
| Nav style | Simple sticky bar, inline styles | Full nav with blur backdrop, `css/styles.css` classes |
| Max width | 800px article | 1140px via `.container` |
| Font load | `@import` in `<style>` | `<link>` tag to Google Fonts |
| Demo booking | `href="https://www.goswirl.ai"` button | Calendly popup widget |
| Footer | None (related articles + CTA) | Full `<footer>` with nav links |

**Rule:** Never apply article-page CSS patterns to homepage sections or vice versa. They are separate systems.

---

### B.2 Shared Stylesheet — `css/styles.css`

The homepage and product/concept pages all load `<link rel="stylesheet" href="css/styles.css">`. Do not inline CSS on these pages — add it to `css/styles.css` instead.

**CSS custom properties (design tokens) in `css/styles.css`:**

```css
:root {
  --white: #FFFFFF;
  --bg-primary: #FFFFFF;
  --bg-soft: #f4f3ec;         /* warm off-white — section alt backgrounds */
  --bg-warm: #f4f3ec;
  --bg-dark: #0B1D2C;         /* dark section backgrounds */
  --bg-dark-mid: #122A3D;
  --bg-card: #FFFFFF;

  --border-light: #EBEBEB;
  --border-medium: #D4D4D4;

  --text-primary: #111111;
  --text-secondary: #555555;
  --text-muted: #888888;
  --text-on-dark: #FFFFFF;
  --text-on-dark-muted: rgba(255,255,255,0.65);

  --accent: #111111;
  --teal: #000281;             /* primary brand color — buttons, highlights, links */
  --teal-light: #00028133;

  --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius: 12px;
  --radius-sm: 8px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --max-width: 1140px;
  --transition: 0.25s ease;
}
```

Note: The homepage uses `--bg-dark: #0B1D2C` and `--teal: #000281`. Article pages use `#0F0A3C` for headings and `#2D1B8E` for links. These are different — do not mix them.

---

### B.3 Navigation — Homepage / Product Pages

The homepage uses the full nav from `css/styles.css`, not the inline blog nav.

**HTML pattern:**
```html
<nav aria-label="Main navigation">
  <div class="nav-inner">
    <a href="/" class="nav-logo" aria-label="Swirl Home">
      <img src="assets/logo.svg" alt="Swirl" width="90" height="26">
    </a>
    <div class="nav-links" role="menubar">
      <a href="#how-it-works" role="menuitem">How It Works</a>
      <a href="#nudges" role="menuitem">Product</a>
      <a href="agentic-commerce.html" role="menuitem">Agentic Commerce</a>
      <a href="ai-sales-agent.html" role="menuitem">AI Sales Agent</a>
      <a href="touchless-commerce.html" role="menuitem">Touchless Commerce</a>
      <a href="blog.html" role="menuitem">Blog</a>
      <a href="javascript:void(0)" onclick="Calendly.initPopupWidget({url:'https://calendly.com/prashant-ramani/30min'});return false;" class="nav-cta">Book a Demo</a>
    </div>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle mobile menu" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<!-- Mobile Menu -->
<nav class="mobile-menu" id="mobileMenu" aria-label="Mobile navigation">
  <a href="#how-it-works" class="mobile-link">How It Works</a>
  <a href="#nudges" class="mobile-link">Product</a>
  <a href="agentic-commerce.html" class="mobile-link">Agentic Commerce</a>
  <a href="ai-sales-agent.html" class="mobile-link">AI Sales Agent</a>
  <a href="touchless-commerce.html" class="mobile-link">Touchless Commerce</a>
  <a href="blog.html" class="mobile-link">Blog</a>
  <a href="javascript:void(0)" onclick="Calendly.initPopupWidget({url:'https://calendly.com/prashant-ramani/30min'});return false;" class="mobile-cta">Book a Demo</a>
</nav>
```

**Required JS for mobile toggle** (bottom of `<body>`):
```html
<script>
  const navToggle = document.getElementById('navToggle');
  const mobileMenu = document.getElementById('mobileMenu');
  navToggle.addEventListener('click', () => {
    const isOpen = mobileMenu.classList.toggle('open');
    navToggle.classList.toggle('open', isOpen);
    navToggle.setAttribute('aria-expanded', isOpen);
  });
  document.querySelectorAll('.mobile-menu a').forEach(link => {
    link.addEventListener('click', () => {
      mobileMenu.classList.remove('open');
      navToggle.classList.remove('open');
      navToggle.setAttribute('aria-expanded', false);
    });
  });
</script>
```

**Required in `<head>`** for Calendly (homepage and product pages only):
```html
<link href="https://assets.calendly.com/assets/external/widget.css" rel="stylesheet">
<script src="https://assets.calendly.com/assets/external/widget.js" type="text/javascript" async></script>
```

**Calendly URL:** `https://calendly.com/prashant-ramani/30min` — use this everywhere the demo CTA appears on homepage/product pages.

---

### B.4 Homepage Schema (index.html only)

The homepage uses 5 schema blocks, not 4. Order matters.

1. **Organization** — same as article pages (see Step 4.1)
2. **WebSite** — with `hasPart` listing every page on the site
3. **WebPage** — with `speakable` CSS selectors
4. **SoftwareApplication** — describes Swirl as a product with `featureList`
5. **HowTo** — Swirl's 4-step process (Nudges → Speaks → Acts → Learns)
6. **FAQPage** — 10 questions covering what Swirl is, pricing, deployment, differentiators

**When adding a new page to the site, update the `hasPart` array in the WebSite schema in `index.html`.**

---

### B.5 Homepage Sections — Structure and Classes

The homepage is divided into named sections. Each uses `.section` (100px padding) or `.section.alt` (same + `var(--bg-soft)` background). All content sits inside `.container` (max-width 1140px).

**Section map in order:**

| Section | `id` | Class | Purpose |
|---|---|---|---|
| Hero | `hero-heading` | `.hero` | Headline + CTA buttons |
| Logo bar | — | `.logo-bar` | Animated client logo scroll |
| Watch it work | — | `.watch-section` | YouTube demo video with lazy thumbnail |
| What is Swirl | `what-is-swirl` | `.section` | Definition block |
| Commerce is changing | `problem` | `.problem-section` | 4-card problem grid |
| How Swirl works | `how-it-works` | `.section.alt` | 4 step-cards (Nudges/Speaks/Acts/Learns) |
| Where buyers drop off | `drop-off` | `.section` | 4-card conversion funnel |
| Deep dive (product) | `nudges` | `.section` | `.deep-row` pairs with visual + feature list |
| Trained on signals | `trained` | `.section.alt` | Signal card + comparison grid |
| Key concepts | — | `.section` | `.benefits-grid` of 3 concept cards |
| Metrics / proof | — | `.section.alt` | Stats + BYD case study highlight |
| FAQ | `faq-heading` | `.section` | 10-question FAQ |
| Footer | — | `<footer>` | Logo + nav links + copyright |

**Key CSS classes for homepage sections:**

```
.hero                    — hero section wrapper (padding: 140px 0 80px)
.hero-inner              — centered content, max-width 780px
.hero-badge              — small pill badge above H1
.hero-sub                — subtitle paragraph
.hero-ctas               — flex row of CTA buttons
.btn-primary             — navy pill button (--teal background)
.btn-secondary           — outlined pill button
.highlight               — inline color highlight (--teal) inside headings

.logo-bar                — client logo scroll section
.logo-bar-label          — "Trusted by leading brands" uppercase label
.logo-track              — animates with logo-scroll keyframe (28s linear infinite)
.logo-bar-img            — greyscale logos, color on hover

.watch-section           — video section wrapper
.video-wrapper           — 16:9 aspect-ratio box, border-radius: --radius-xl
.video-thumbnail         — absolute-fill thumbnail image
.video-play-btn          — centered circular play button

.section                 — standard section (padding: 100px 0)
.section.alt             — same + var(--bg-soft) background
.section-header          — centered header block (margin-bottom: 56px)
.section-label           — small pill label above section heading
.section-title           — H2, clamp(30px,3.5vw,44px), font-weight 800
.section-sub             — subtitle under section heading

.problem-section         — commerce-is-changing section (padding: 100px 0)
.problem-header          — centered header
.problem-grid            — 2-col grid, max-width 800px
.problem-card            — individual problem card
.problem-icon            — 44×44 icon container

.steps-grid              — 4-col grid for Nudges/Speaks/Acts/Learns step cards
.step-card               — individual step card (not the same as .step in articles)
.step-icon               — product screenshot image in step card
.step-name               — bold step name
.step-desc               — step description

.deep-row                — 2-col feature row (text left + visual right)
.deep-row.flip           — reverses order (visual left + text right)
.deep-step-label         — "Step N — Name" label
.deep-title              — H3 inside deep-row
.deep-desc               — paragraph under deep-title
.deep-features           — feature list (ul)
.feat-icon               — SVG icon circle
.feat-text               — feature label + description
.deep-visual             — right-side visual container

.benefits-grid           — 3-col grid of concept cards
.benefit-card            — individual concept card
.card-num                — "01 / 02 / 03" label in teal
.card-link               — "Learn more →" link in teal

.site-footer             — full footer wrapper
.site-footer-inner       — centered inner (max-width 1100px)
.footer-logo             — Swirl logo in footer
.footer-links            — horizontal nav links
.footer-copy             — copyright line
```

---

### B.6 Hero Section Pattern

```html
<section class="hero" aria-labelledby="hero-heading">
  <div class="container">
    <div class="hero-inner">
      <div class="hero-badge"><span class="dot"></span> [Badge text]</div>
      <h1 id="hero-heading">[Main headline]<br>[with] <span class="highlight">[highlighted word]</span></h1>
      <p class="hero-sub">[Subtitle — 1–2 sentences, max 600px wide]</p>
      <div class="hero-ctas">
        <a href="javascript:void(0)" onclick="Calendly.initPopupWidget({url:'https://calendly.com/prashant-ramani/30min'});return false;" class="btn-primary">Book a Demo &rarr;</a>
        <a href="#[anchor]" class="btn-secondary">[Secondary action]</a>
      </div>
    </div>
  </div>
</section>
```

**Current hero headline:** "Hire an AI Sales Force that sells **24/7**"
**Current hero subtitle:** "Every buyer gets a personal AI guide from **which product is right for me?** to checkout. No wait times. No drop-offs. No human required."

Only change these if the core value proposition changes. Do not rewrite hero copy for a single blog campaign.

---

### B.7 Logo Bar Pattern

```html
<section class="logo-bar" aria-label="Trusted brands">
  <div class="container">
    <div class="logo-bar-label">Trusted by leading brands</div>
    <div class="logo-bar-logos">
      <div class="logo-track">
        <!-- Real logos with alt text -->
        <img src="assets/lg.png" alt="LG" class="logo-bar-img">
        <img src="assets/byd.png" alt="BYD" class="logo-bar-img">
        <img src="assets/al-badia.png" alt="Al Badia" class="logo-bar-img">
        <img src="assets/al-futtaim.png" alt="Al-Futtaim Group" class="logo-bar-img">
        <img src="assets/denza.png" alt="Denza" class="logo-bar-img">
        <img src="assets/yang-wang.png" alt="Yangwang" class="logo-bar-img">
        <img src="assets/vivo.png" alt="Vivo" class="logo-bar-img">
        <!-- Duplicate set for seamless loop — aria-hidden -->
        <img src="assets/lg.png" alt="" class="logo-bar-img" aria-hidden="true">
        <!-- ... repeat all logos with aria-hidden="true" ... -->
      </div>
    </div>
  </div>
</section>
```

The animation is a CSS keyframe (`logo-scroll`, 28s linear infinite) in `css/styles.css`. To add a new client logo: add the real logo file to `assets/`, add it to both the real set and the duplicate set.

---

### B.8 Section Header Pattern (Reusable)

```html
<div class="section-header">
  <div class="section-label">[CATEGORY LABEL]</div>
  <h2 class="section-title" id="[section-id]-heading">[Section heading with optional <span class="highlight">highlight</span>]</h2>
  <p class="section-sub">[One-line subtitle, max 540px]</p>
</div>
```

---

### B.9 Problem / Insight Grid Pattern

Use `.problem-grid` for 2×2 grids of insight or problem cards. Use `.benefits-grid` for 3-col concept or feature cards.

```html
<!-- 2-col problem grid -->
<div class="problem-grid">
  <div class="problem-card fade-in">
    <div class="problem-icon" aria-hidden="true">
      <img src="assets/[icon].png" alt="[description]" width="22" height="22">
    </div>
    <p><strong>[Bold lead]</strong> [Supporting sentence]</p>
  </div>
</div>

<!-- 3-col benefit/concept grid -->
<div class="benefits-grid">
  <div class="benefit-card">
    <span class="card-num">01</span>
    <h3><a href="[page].html">[Concept title]</a></h3>
    <p>[Description]</p>
    <a href="[page].html" class="card-link">Learn more →</a>
  </div>
</div>
```

---

### B.10 Footer Pattern

```html
<footer class="site-footer">
  <div class="site-footer-inner">
    <a href="index.html" class="footer-logo" aria-label="Swirl Home">
      <img src="assets/logo.svg" alt="Swirl" width="90" height="26">
    </a>
    <div class="footer-links">
      <a href="index.html">Home</a>
      <a href="ai-sales-agent.html">AI Sales Agent</a>
      <a href="agentic-commerce.html">Agentic Commerce</a>
      <a href="case-study-byd-ai-sales-agent.html">Case Study</a>
      <a href="blog.html">Blog</a>
    </div>
    <p class="footer-copy">© 2026 Swirl. All rights reserved.</p>
  </div>
</footer>
```

When adding a new page, decide whether it belongs in the footer nav. Only high-authority pages go here — not every blog post.

---

### B.11 Blog Index Page (`blog.html`)

The blog index uses its own inline CSS (not `css/styles.css`) plus loads `css/styles.css` for the nav. Key classes:

```
.blog-hero          — hero header section (padding: 72px 24px 48px, max-width 1100px)
.blog-hero-label    — "Swirl Blog" uppercase label in --teal (#2D1B8E)
.filter-bar         — horizontal filter tab row
.filter-btn         — pill filter button; .active = navy fill
.blog-grid          — auto-fill grid (minmax 320px), gap 32px, max-width 1100px
.blog-card          — article card with border, border-radius 12px
.blog-card.featured — full-width featured card (flex-direction: row, background #F8F7FF)
.card-tag           — "CATEGORY · Type" label in #2D1B8E
.card-title         — Playfair Display headline
.card-desc          — body description
.card-meta          — read time + date + author row
.card-arrow         — "Read article →" link
.featured-badge     — "★ Featured Case Study" dark pill
.stats-row          — flex row of stat cells inside featured card
.stat-num           — large Playfair number
.stat-lbl           — small label under stat-num
```

**Adding a new article to the blog index:**
```html
<a href="[slug].html" class="blog-card">
  <span class="card-tag">[CATEGORY · Type]</span>
  <p class="card-title">[Article title]</p>
  <p class="card-desc">[1–2 sentence description — what the article covers and why it matters]</p>
  <div class="card-meta">
    <span>[X min read]</span>
    <span class="card-meta-dot"></span>
    <span>[Month Year]</span>
    <span class="card-meta-dot"></span>
    <span>By [Author]</span>
  </div>
  <span class="card-arrow">Read [article/guide/case study] →</span>
</a>
```

Insert new cards in reverse chronological order (newest first), after the featured card.

**Card tag categories in use:**
- `Automotive AI · Guide` / `· Case Study` / `· How-To` / `· Comparison` / `· Opinion` / `· Explainer`
- `Agentic Commerce · Guide` / `· Framework` / `· Explainer`
- `Technology · Architecture`
- `Industry Guide · Consumer Electronics` / `· Retail` / `· D2C` / `· Healthcare`

---

### B.12 Homepage Schema — When to Update

Every time you add a new page to the site, open `index.html` and add it to the `hasPart` array inside the WebSite schema:

```json
{"@type": "WebPage", "url": "https://www.goswirl.ai/[slug]", "name": "[Page title]"}
```

Also update the `dateModified` field in the WebPage schema to the current date.

---

### B.13 Homepage Messaging — What Not to Change Without Context

These are the current approved claims on the homepage. Do not change numbers, update the tagline, or modify the hero without checking they are still accurate.

| Claim | Location |
|---|---|
| "Hire an AI Sales Force that sells 24/7" | Hero H1 |
| "The Touchless Commerce OS" | Hero badge, title tag |
| 13% Conversion Rate | Metrics section, FAQ schema |
| 28% Engagement Rate | Metrics section, FAQ schema |
| 75% increase in time on site | FAQ schema |
| 2.5× MoM AI session growth | FAQ schema |
| 50+ languages | Nav badge, FAQ schema, product section |
| "Go live in 2 weeks" | Nav CTA context, FAQ schema, footer context |
| 100M+ real customer signals | Trained-on section |
| Calendly URL: `calendly.com/prashant-ramani/30min` | All demo CTAs on homepage |

---

## Quick Reference: AEO Good vs Bad

| Good | Bad |
|---|---|
| "In the BYD Al-Futtaim deployment, Swirl achieved 27% engagement" | "Our AI achieves industry-leading engagement" |
| "BDC turnover exceeds 60% annually in automotive" | "BDC turnover is very high" |
| FAQ answer that is a complete paragraph standing alone | FAQ answer that says "As mentioned above..." |
| H2: "Why Is Automotive BDC Turnover So High?" | H2: "The Problem" |
| Stats grid with 4 specific metrics and sources | Bullet list of vague capabilities |
| HowTo schema with exact steps and durations | Article schema only on a how-to page |
| AEO hidden section with every named stat from the page | AEO hidden section with a 2-line summary |
| `about` entity links to Wikipedia in Article schema | Article schema with no entity linking |
