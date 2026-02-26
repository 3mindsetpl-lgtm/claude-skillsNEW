
# CRO Frameworks Reference

Detailed frameworks for conversion rate optimization across all touchpoints.

## Table of Contents
1. [Page CRO Analysis](#page-cro-analysis)
2. [Signup Flow CRO](#signup-flow-cro)
3. [Onboarding CRO](#onboarding-cro)
4. [Form CRO](#form-cro)
5. [Popup/Modal CRO](#popup-modal-cro)
6. [Paywall/Upgrade CRO](#paywall-upgrade-cro)

---

## Page CRO Analysis

### Full Analysis Framework

Analyze in this order (highest to lowest impact):

#### 1. Value Proposition Clarity (5-Second Test)
- Can a visitor understand what this is and why they should care within 5 seconds?
- Is the headline specific and benefit-oriented (not feature-oriented)?
- Does the subheadline add concrete detail or expand the promise?
- Is the primary CTA visible and clear above the fold?
- Is there a visual that supports the message (product screenshot, demo, illustration)?

#### 2. Social Proof & Trust
- Are logos, testimonials, or case studies present?
- Is social proof *specific*? ("2,400+ teams" beats "Trusted by many")
- Are testimonials attributed with name, title, company?
- Is social proof placed near CTAs (not buried at bottom)?
- Are there trust signals? (security badges, guarantees, privacy notes)

#### 3. Friction Reduction
- Can visitors complete the primary action with minimal steps?
- Are there unnecessary form fields?
- Is there clear risk reversal? (free trial, money-back guarantee, no credit card)
- Are objections addressed before/near the CTA?
- Is the commitment level clear? (what happens after they click?)

#### 4. Information Architecture
- Does the page tell a story? Problem → Solution → Proof → CTA
- Is there clear visual hierarchy (F-pattern or Z-pattern)?
- Is the most important content above the fold?
- Are there multiple CTA placements (top, middle, bottom)?
- Is there logical primary vs. secondary CTA structure?

#### 5. Mobile Experience
- Is all critical content visible without horizontal scrolling?
- Are CTAs thumb-friendly and easy to tap?
- Does the page load fast? (<3 seconds)
- Is text readable without zooming?

### Page-Type-Specific Priorities

**Homepage**
- Serve multiple audiences without being generic
- Lead with broadest value proposition
- Clear navigation paths for different visitor intents
- Social proof from recognizable names

**Landing Page**
- Single message, single CTA — no navigation menu
- Headline matches the ad/traffic source
- Complete argument on one page
- Stronger risk reversal language

**Pricing Page**
- Help visitors choose the right plan
- Make recommended plan obvious (visual highlight, "Most Popular" badge)
- Address "which is right for me?" anxiety
- Include FAQ addressing common pricing objections
- Show annual/monthly toggle with annual savings highlighted

**Feature Page**
- Feature → Benefit → Outcome chain
- Show use cases with screenshots or demos
- Compare against doing it manually or with alternatives
- Clear path to try or buy

---

## Signup Flow CRO

### Core Principles
- Every additional step loses ~20% of users
- Delay non-essential fields until after initial signup
- Show progress indicators for multi-step flows
- Match friction level to product value

### Field Priority
**Required first**: Email only, or email + password
**Delay until needed**: Name, company, phone, role
**Skip entirely**: Address, birthday, "how did you hear about us" (use UTMs instead)

### SSO Priority (by conversion impact)
1. Google — highest conversion lift for most B2B/B2C
2. Microsoft — for enterprise-focused products
3. GitHub — for developer tools
4. Apple — for consumer products
5. Email/password — always available as fallback

### Post-Signup Optimization
- Immediately show value (don't redirect to empty dashboard)
- First screen should guide to the key action
- Use progressive profiling to collect info over time
- Send welcome email within 1 minute

---

## Onboarding CRO

### Key Metrics
- Activation rate: % of signups who reach "aha moment"
- Time to first value: how long until first meaningful outcome
- Feature adoption: which features drive retention

### Onboarding Patterns
1. **Checklist**: 3-5 key tasks to complete (show progress)
2. **Guided tour**: Step-by-step walkthrough of core features
3. **Template/sample data**: Pre-populate with examples so it's not empty
4. **Quick win**: Guide to the single fastest path to value

### Empty State Strategy
Never show a blank screen. For each empty state:
- Show what it will look like with data
- Provide a clear single action to get started
- Offer templates, examples, or import options

---

## Form CRO

### Field Optimization
- Remove every field that isn't strictly necessary
- Use smart defaults and auto-detection (country from IP, etc.)
- Single-column layout (don't put fields side-by-side)
- Group related fields logically
- Inline validation (show errors as user types, not on submit)

### Form Types & Best Practices

**Lead Capture**
- 1-3 fields maximum (email, maybe name + company)
- Strong value proposition above the form
- Clear what they'll receive and when

**Contact/Sales**
- Name, email, company, message (4 fields max)
- Show expected response time
- Offer alternative contact methods (chat, phone)

**Survey/Feedback**
- Progress bar for multi-step
- Most important questions first
- Allow partial completion (save progress)

### Mobile Form Rules
- Larger touch targets (44px minimum)
- Show appropriate keyboard type per field
- Sticky submit button at bottom
- Auto-focus first field on page load

---

## Popup/Modal CRO

### Popup Types by Purpose
| Type | Trigger | Use Case |
|------|---------|----------|
| Exit-intent | Mouse toward close/back | Save abandoning visitors |
| Time-delayed | After X seconds | Capture engaged visitors |
| Scroll-depth | After X% scroll | Target interested readers |
| Click-triggered | Button/link click | Opt-in driven |

### Best Practices
- Only show one popup per session
- Easy to close (visible X, click outside to close)
- Mobile-friendly (full-screen takeover or bottom sheet)
- Clear value exchange (what they get for their email)
- Don't show to returning visitors who've already dismissed

### Exit-Intent Popup Framework
1. **Headline**: Address why they're leaving or make a compelling offer
2. **Body**: 1-2 sentences, focus on what they'll miss
3. **CTA**: Specific action ("Get the Free Guide" not "Subscribe")
4. **Discount/bonus**: If appropriate, offer something exclusive

---

## Paywall/Upgrade CRO

### When to Show Upgrade Prompts
- User hits a feature limit (natural moment of need)
- User has been active for X days/sessions (invested in product)
- User tries to access a premium feature
- User's usage is growing (they're getting value)

### Upgrade Screen Framework
1. **Acknowledge current usage**: "You've created 10 projects this month!"
2. **Show what they're missing**: Specific features or limits they'll unlock
3. **Social proof**: What similar users achieved after upgrading
4. **Clear pricing**: Show exact price, billing period, any discounts
5. **Risk reversal**: Free trial period, money-back guarantee

### Pricing Display
- Highlight the recommended plan visually
- Show per-month pricing (even for annual billing)
- Display annual savings as a percentage or dollar amount
- Include feature comparison between current and upgrade tier
- Add "Contact sales" for enterprise (don't hide it)
