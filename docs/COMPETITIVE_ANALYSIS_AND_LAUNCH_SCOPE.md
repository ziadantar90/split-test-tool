# Competitive analysis & launch scope

**Product:** Self-serve website A/B testing (split testing)  
**Positioning:** Bottom-up SaaS for small teams and marketers — not enterprise. Target ~$49–99/month vs. quote-based incumbents.  
**Last updated:** September 2025  
**Sources:** Public marketing pages, G2/Capterra/Trustpilot/AWS Marketplace reviews, and third-party pricing roundups (verify pricing before sales decisions).

---

## 1. Who we compare to (closest, non-enterprise)

| Competitor | Why they’re close | Why they’re *not* our exact clone |
|------------|-------------------|-----------------------------------|
| [Convert](https://www.convert.com/) | Privacy-focused A/B testing, mid-market sweet spot, strong reviews on support & editor | Annual contracts, session-based pricing scales up |
| [VWO](https://vwo.com/) | Classic “add snippet + visual tests” playbook | Sales-led pricing, heavy suite, frequent complaints on cost & data trust |
| [Omniconvert Explore](https://www.omniconvert.com/) | Free tier on real traffic (50k tested visitors), visual editor, ecommerce CRO | Ecommerce-first; paid tiers climb quickly; feature breadth = complexity |
| [GrowthBook](https://www.growthbook.io/) | Affordable experimentation for startups | Warehouse/dev-first; weak fit for non-technical marketers alone |
| [PostHog](https://posthog.com/experiments) | Modern self-serve, experiments + flags | You must adopt their analytics stack; experiments are one module among many |

**Out of scope for “closest” (enterprise / wrong buyer):** [Optimizely](https://www.optimizely.com/), [AB Tasty](https://www.abtasty.com/) (quote-only, often €15k+/year), [Adobe Target](https://business.adobe.com/products/target/adobe-target.html).

**Historical gap we’re filling:** [Google Optimize](https://support.google.com/optimize/answer/12979939) (discontinued) left small sites without a simple, cheap split-testing tool.

---

## 2. Best qualities to learn from (by competitor)

### Convert

**What users praise**

- Strong **visual/WYSIWYG editor** and ability to run many test types without developers ([G2 comparison vs VWO](https://www.g2.com/compare/convert-experiences-vs-wingify-vwo-testing)).
- **Reporting & analytics** rated highly vs peers on G2.
- **Support quality** (often cited as a differentiator).
- **Performance / low flicker** and **privacy/GDPR positioning** ([review roundup](https://marketingtoolpro.com/convert-com-review/)).
- Clear-ish **session-based pricing** (predictable vs opaque quotes).

**Takeaway for us:** Nail **fast, flicker-aware snippet**, **honest stats**, and **responsive support** even at low ARPU.

---

### VWO

**What users praise (when it works)**

- **All-in-one CRO** (tests, heatmaps, surveys, recordings) in one vendor.
- **Mature visual editor** for marketers (when pages aren’t too dynamic).
- **Brand recognition** and onboarding/sales experience (pre-purchase).

**Takeaway for us:** Don’t try to match the full suite at launch. Copy the **“install snippet → create test in UI → see winner”** workflow, not the product breadth.

---

### Omniconvert Explore

**What users praise**

- **Generous free tier on real traffic** (50k tested visitors, no time-limited trial clock) ([pricing FAQ](https://www.omniconvert.com/pricing/)).
- **Full platform on free tier**, not a crippled demo.
- **Bayesian + frequentist** stats, segmentation, visual + code editors.
- Strong **ecommerce use cases** (pricing, shipping, PDP tests).

**Takeaway for us:** **Traffic-based free tier** or long “proof” allowance is a powerful GTM wedge for concept validation.

---

### GrowthBook

**What users praise**

- **Warehouse-native** results (single source of truth with your analytics).
- **Rigorous statistics** (Bayesian, CUPED, sequential) and **lightweight SDKs**.
- **Open source / self-host** option and fair cloud pricing for technical teams ([reviews](https://aws.amazon.com/marketplace/reviews/reviews-list/prodview-2ltf7dt5g2y6q)).

**Takeaway for us:** Offer **simple, trustworthy primary metrics** first; add depth later. Optional **export/API** for technical users without requiring a warehouse day one.

---

### PostHog

**What users praise**

- **Experiments tied to feature flags** and existing event taxonomy ([docs](https://posthog.com/docs/experiments)).
- **Session replays per variant** (qualitative “why” after quantitative “what”).
- **Self-serve signup**, transparent culture, dev-friendly docs.

**Takeaway for us:** Link **one primary goal** clearly in the UI; consider **replay integration** (PostHog, Clarity, etc.) in Phase 2 instead of building recordings.

---

## 3. Negative reviews & gaps → our opportunities

Themes repeated across **Convert, VWO, Omniconvert, GrowthBook, PostHog** (small-business and mid-market reviewers). Use these as explicit product/marketing promises.

| Pain theme | Typical complaint | Our opportunity |
|------------|-------------------|-----------------|
| **Opaque / rising price** | VWO/AB Tasty quote-only; VWO MTU jumps; Convert annual-only ([Convert review](https://marketingtoolpro.com/convert-com-review/)) | **Published monthly price**, month-to-month, clear MTU/session cap on site |
| **Paywall on your own data** | VWO: configure tests then can’t see key reports without upgrade ([Trustpilot](https://www.trustpilot.com/review/vwo.com)) | **No bait-and-switch**: core results on every paid tier; one clear upgrade dimension (traffic) |
| **Don’t trust the numbers** | VWO tracking vs manual counts; flicker/speed skew ([Trustpilot](https://www.trustpilot.com/review/vwo.com), [FinancesOnline cons](https://reviews.financesonline.com/p/visual-website-optimizer/)) | **SRM checks**, exposure logging, simple **A/A test** guide; performance budget for snippet |
| **Editor breaks on modern sites** | Glitchy editor on SPAs/dynamic layouts (VWO, AB Tasty) | Launch with **URL split + element text/CSS** first; document SPA limitations honestly |
| **Too complex for marketers** | GrowthBook/PostHog need instrumentation; Convert advanced rules need docs | **Opinionated wizard**: one page, two variants, one goal — defaults that work |
| **Annual lock-in** | Convert annual contracts | **Monthly billing** from day one (Stripe) |
| **Suite overload** | Heatmaps, surveys, personalization sold as bundle | **Do one job well**: A/B tests + conversions; integrate for the rest |
| **Support / cancellation friction** | VWO billing/cancellation stories ([review aggregators](https://piperocket.digital/review/vwo-reviews/)) | Self-serve **cancel in app**; status page; async support with SLA on paid tier |
| **Implementation gotchas** | PostHog: flag evaluated too late → wrong splits ([troubleshooting](https://posthog.com/docs/experiments/troubleshooting)) | **Install checker** in dashboard (“snippet seen”, “goal firing”, sample exposure) |
| **Stats confusion** | Multiple metrics → false positives (PostHog docs); GrowthBook stats learning curve | **One primary metric** required; plain-language winner call; advanced stats later |

### Positioning sentence (internal)

> “Google Optimize simplicity + Convert-grade testing workflow + honest pricing — without enterprise sales, warehouse setup, or full analytics migration.”

---

## 4. What we are *not* building first

To stay bottom-up and provable:

- Enterprise SSO, SCIM, dedicated CSM, multi-region contracts  
- Full CRO suite (heatmaps, session replay, surveys, personalization engine)  
- Server-side / mobile SDK parity  
- Multivariate, bandits, holdouts, fake-door tests  
- Visual drag-and-drop editor on every framework (especially SPAs)  
- Warehouse-native-only analytics (GrowthBook model)

---

## 5. Launch package — smallest shippable product to prove the concept

**Goal:** A paying (or strongly activated free) customer can run **one real A/B test** on their marketing site, see **exposures + conversions per variant**, and decide **winner vs keep running** — without calling sales.

**Name:** **Launch v0** (concept proof; not the long-term “full MVP”).

### 5.1 Customer journey (Launch v0)

1. **Sign up** (email + password or Google OAuth).  
2. **Create project** (site name + primary domain).  
3. **Install snippet** — copy/paste one `<script>` (or GTM tag). Dashboard shows: installed ✓, last event received.  
4. **Create experiment** (wizard):  
   - Page URL match (exact or simple prefix)  
   - **Control vs one variant** (A/B only)  
   - Variant change: **text replace** OR **CSS** OR **redirect URL** (pick 1–2 mechanisms max)  
   - **One primary goal**: click selector OR pageview URL OR custom event name  
   - Traffic split 50/50 (fixed)  
5. **Start / pause** experiment.  
6. **Results page**: impressions per variant, conversions, conversion rate, simple significance indicator (frequentist or Bayesian — pick one and document it).  
7. **Upgrade** when over free session cap (Stripe Checkout).

### 5.2 What we build (our side)

| Component | Launch v0 scope |
|-----------|-----------------|
| **Marketing site** | Single landing: problem, pricing, sign up CTA |
| **Auth** | Sign up, login, password reset |
| **Billing** | Stripe: **one paid plan** + **free tier** (e.g. 10k–25k tested sessions/mo); monthly |
| **Dashboard** | Projects, experiments list, create/edit wizard, results |
| **Snippet (JS)** | Stable variant assignment (cookie/localStorage), apply DOM changes, send exposure + conversion beacons |
| **API + DB** | Experiments, variants, goals, events aggregation (batch or stream) |
| **Admin** | Minimal internal view for support (account lookup, event counts) |

### 5.3 Explicit Launch v0 limits (communicate on website)

- 1 project, 1 active experiment (or 3 total experiments) on free tier  
- A/B only (no A/B/n)  
- Web only, client-side snippet  
- No team seats / roles (single user)  
- No visual point-and-click editor (form-based changes only)  
- English UI only  

These limits are **features for focus**, not apologies.

### 5.4 Success metrics (concept proof)

| Metric | Target (first 90 days) |
|--------|-------------------------|
| Activated accounts | Snippet firing on live site |
| Experiments started | ≥1 per activated account (median) |
| Experiments completed | User viewed results with ≥1k exposures/variant (guidance in UI) |
| Revenue | First 5–10 paying customers OR clear conversion free → paid |
| Qualitative | Users cite “easy install” and “I trust the numbers” in interviews |

---

## 6. Phase roadmap (after Launch v0)

**Phase 1 — MVP proper (~“lowest full product”)**

- 3+ concurrent experiments  
- Simple **visual editor** for static pages (or Chrome extension)  
- **Secondary metrics** (max 2)  
- Email alerts (experiment reached significance / broken install)  
- Team: 2–3 seats  

**Phase 2 — Growth**

- A/B/n, split-URL tests at scale, mutual exclusion groups  
- Integrations: GA4, Segment, Webflow, WordPress plugin  
- Shopify-specific onboarding (compete with Omniconvert wedge)  
- Session replay link-outs  

**Phase 3 — Optional “upmarket”**

- Server-side bucketing API  
- Feature flags lite  
- SSO (only when customers ask)

---

## 7. Pricing sketch (align with gaps)

| Tier | Price (target) | Traffic | Purpose |
|------|----------------|---------|---------|
| **Free** | $0 | 10k–25k tested sessions/mo | Prove value; no time bomb (learn from Omniconvert) |
| **Starter** | $49/mo | ~50k sessions | Solo marketer / indie SaaS |
| **Growth** | $99/mo | ~150k sessions | Small team, 3 seats |

**Rules:** Prices on website; monthly cancel; overage = soft cap + email upgrade (don’t silently pause tests without warning — VWO complaint theme).

---

## 8. Competitor links (quick reference)

- Convert — https://www.convert.com/  
- VWO — https://vwo.com/  
- Omniconvert — https://www.omniconvert.com/  
- GrowthBook — https://www.growthbook.io/  
- PostHog Experiments — https://posthog.com/experiments  
- Google Optimize (sunset) — https://support.google.com/optimize/answer/12979939  

**Review hubs (for ongoing monitoring):**

- G2 A/B Testing category — https://www.g2.com/categories/a-b-testing  
- Convert vs VWO — https://www.g2.com/compare/convert-experiences-vs-wingify-vwo-testing  
- VWO Trustpilot — https://www.trustpilot.com/review/vwo.com  

---

## 9. Document maintenance

- Re-scan G2/Trustpilot quarterly for new complaint clusters.  
- Re-verify competitor pricing pages before any public pricing change.  
- When Launch v0 ships, tick off scope in §5.2 and move deferred items to Phase 1.
