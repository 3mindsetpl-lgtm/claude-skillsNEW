
# SEO Guide Reference

Detailed frameworks for SEO audits, programmatic SEO, schema markup, and competitor pages.

## Table of Contents
1. [SEO Audit Framework](#seo-audit-framework)
2. [Programmatic SEO](#programmatic-seo)
3. [Schema Markup](#schema-markup)
4. [Competitor & Alternative Pages](#competitor-alternative-pages)
5. [Content Strategy](#content-strategy)

---

## SEO Audit Framework

### Audit Order (by impact)

#### 1. Crawlability & Indexation
- Is robots.txt properly configured?
- Is the sitemap.xml present, submitted, and up-to-date?
- Are important pages indexable (no accidental noindex)?
- Are there crawl errors in Search Console?
- Is the site using canonical tags correctly?

#### 2. On-Page SEO
- **Title tags**: Unique, keyword-inclusive, 50-60 characters, compelling
- **Meta descriptions**: Unique, action-oriented, 150-160 characters
- **H1 tags**: One per page, matches primary keyword intent
- **Header hierarchy**: Logical H1 → H2 → H3 structure
- **Internal linking**: Key pages linked from navigation and content
- **URL structure**: Clean, descriptive, keyword-inclusive

#### 3. Content Quality
- Is content unique and valuable (not thin or duplicated)?
- Does it match search intent for target keywords?
- Is it comprehensive enough to satisfy the query?
- Are there content gaps vs. ranking competitors?
- Is content fresh and up-to-date?

#### 4. Technical Performance
- **Page speed**: Core Web Vitals (LCP < 2.5s, FID < 100ms, CLS < 0.1)
- **Mobile-friendliness**: Passes Google mobile-friendly test
- **HTTPS**: Entire site on HTTPS with proper redirects
- **Structured data**: Schema markup for relevant content types
- **Broken links**: No 404 errors on internal links

#### 5. Off-Page & Authority
- Backlink profile quality and quantity
- Domain authority/rating relative to competitors
- Brand mentions and citations
- Local SEO factors (if applicable)

### Audit Output Format
```
Priority 1 (Critical): Issues blocking indexation or causing major ranking loss
Priority 2 (High): Issues significantly impacting rankings
Priority 3 (Medium): Optimization opportunities
Priority 4 (Low): Nice-to-have improvements
```

### Important Note on Schema Detection
Web fetch/curl strips `<script>` tags (including JSON-LD) and cannot detect JS-injected schema. Always recommend using:
- Google Rich Results Test
- Browser DevTools: `document.querySelectorAll('script[type="application/ld+json"]')`
- Screaming Frog (renders JavaScript)

Never report "no schema found" based solely on HTML source.

---

## Programmatic SEO

### When to Use
- Targeting long-tail keywords at scale
- Data-driven content (locations, comparisons, integrations, use cases)
- Directory-style pages
- Template-based content with variable data

### Page Types
| Type | Template | Example |
|------|----------|---------|
| Location | "{Service} in {City}" | "Plumbers in Austin" |
| Comparison | "{Product A} vs {Product B}" | "Slack vs Teams" |
| Alternative | "{Product} alternatives" | "Salesforce alternatives" |
| Integration | "{Product} + {Integration}" | "Zapier + HubSpot" |
| Use case | "{Product} for {Use Case}" | "Notion for project management" |
| Glossary | "What is {term}" | "What is CRM" |

### Template Requirements
1. **Unique value per page**: Don't just swap the keyword — each page needs unique, useful content
2. **Dynamic data**: Pull in real data (pricing, features, reviews, stats)
3. **Consistent structure**: Same layout, different content
4. **Internal linking**: Cross-link between related pages
5. **Indexation strategy**: Only index pages with sufficient content/value

### Quality Checklist
- [ ] Does each page provide unique value beyond just keyword substitution?
- [ ] Is there real data/content specific to each variation?
- [ ] Would a user find this page genuinely useful?
- [ ] Are there at least 300+ words of meaningful content?
- [ ] Is the page well-structured with proper headings?

---

## Schema Markup

### Priority Schema Types for SaaS/Software

#### Organization Schema (every site)
```json
{
  "@type": "Organization",
  "name": "Company Name",
  "url": "https://example.com",
  "logo": "https://example.com/logo.png",
  "sameAs": ["social media URLs"]
}
```

#### SoftwareApplication (product pages)
```json
{
  "@type": "SoftwareApplication",
  "name": "Product Name",
  "operatingSystem": "Web",
  "applicationCategory": "BusinessApplication",
  "offers": {
    "@type": "Offer",
    "price": "29",
    "priceCurrency": "USD"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "ratingCount": "1200"
  }
}
```

#### FAQPage (any page with FAQ section)
```json
{
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "Question text?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "Answer text."
    }
  }]
}
```

#### BreadcrumbList (all pages)
```json
{
  "@type": "BreadcrumbList",
  "itemListElement": [{
    "@type": "ListItem",
    "position": 1,
    "name": "Home",
    "item": "https://example.com"
  }]
}
```

#### Article (blog posts)
Use for all blog content. Include author, datePublished, dateModified, image.

### Implementation
- Use JSON-LD format (preferred by Google)
- Place in `<head>` or end of `<body>`
- Validate with Google Rich Results Test
- One schema per entity (can have multiple schemas per page)

---

## Competitor & Alternative Pages

### Four Page Formats

#### 1. Singular Alternative ("{Product} alternative")
- Lead with what the user is frustrated about
- Position your product as the solution
- Detailed feature comparison
- Migration/switching guide

#### 2. Plural Alternatives ("{Product} alternatives")
- List 5-10 alternatives (include yourself)
- Be honest about pros/cons of each
- Rank by use case, not "best overall"
- Include pricing comparisons

#### 3. You vs Competitor ("{Your Product} vs {Competitor}")
- Fair, factual comparison
- Use real feature/pricing data
- Acknowledge where competitor excels
- Focus on your differentiators

#### 4. Competitor vs Competitor ("{Competitor A} vs {Competitor B}")
- Objective comparison of two competitors
- Natural mention of your product as an alternative
- Capture informational search intent

### Content Structure for Comparison Pages
1. **Quick summary** — TL;DR comparison table at the top
2. **Overview** of each product (2-3 sentences each)
3. **Feature comparison** — honest, side-by-side table
4. **Pricing comparison** — current, accurate pricing
5. **Pros and cons** of each
6. **Best for** — which use cases each serves best
7. **Your recommendation** — when to choose which
8. **CTA** — subtle pitch for your product

### Important Rules
- Always be factual and honest
- Update pricing and features regularly (quarterly minimum)
- Don't trash competitors — be professional
- Link to competitor websites (shows confidence)
- Include user reviews/quotes when available

---

## Content Strategy

### Content Priorities by Stage

#### Awareness (Top of Funnel)
- "What is {category}?" educational content
- "How to {solve problem}" guides
- Industry trend pieces
- Comparison/best-of posts

#### Consideration (Middle of Funnel)
- Product comparison pages
- Case studies with specific results
- Feature deep-dives
- Webinars and demos

#### Decision (Bottom of Funnel)
- Pricing page optimization
- ROI calculators
- Free trial / demo pages
- Customer testimonials

### Content Calendar Framework
1. **Core pages** (one-time): Homepage, pricing, feature pages, about
2. **Programmatic** (automated): Comparison, alternative, integration pages
3. **Evergreen blog** (monthly): How-to guides, frameworks, best practices
4. **Timely content** (as needed): Industry news, trend analysis, updates

### Keyword Research Process
1. Start with seed keywords (your product category)
2. Expand with "People Also Ask" and related searches
3. Analyze competitor rankings for gaps
4. Prioritize by: search volume × relevance × difficulty
5. Map keywords to content types and funnel stages
