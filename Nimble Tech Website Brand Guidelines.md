# Nimble Tech Website Brand Guidelines

For all public-facing websites under the Nimble Tech header. Currently: BundleRight, FixMyTime. Future tools follow the same system, with their own signature colour.

This document covers websites only. Product UI (the apps themselves) may use a different visual treatment, defined in each product's own brand guide.

---

## 1. Audience and voice

UK law firms and adjacent professional services. Decision-makers (partners, COOs, heads of finance, IT) and the fee-earners who will use the tools day to day.

The voice is calm, precise, and unboastful. Short, declarative sentences. Lead with what the product does for the user, not how it works under the hood. Address the real objection (lock-in, security, change cost) rather than pretending it does not exist.

Rules, no exceptions:

- No exclamation marks.
- Commas over dashes for rhythm. No em dashes anywhere.
- No buzzwords: no "revolutionary", "seamless", "leverage", "synergy", "cutting-edge", "transform".
- Lawyers are spoken to as equals.

---

## 2. Shared visual system

Every Nimble Tech website inherits this base. The only thing that changes per tool is the signature colour (see §3).

### Background palette

| Token | Hex | Use |
|---|---|---|
| `--paper` | `#faf9f7` | Page background, warm off-white |
| `--paper-warm` | `#f3f1ec` | Subtle section break |
| `--paper-mid` | `#e8e4dc` | Card borders, dividers |
| `--ink` | `#0f0e0d` | Primary text, dark CTA section |
| `--ink-mid` | `#4a4845` | Body text |
| `--ink-light` | `#9a9690` | Captions, labels |

### Warn palette (used sparingly, for flagged states only)

| Token | Hex | Use |
|---|---|---|
| `--warn` | `#7a4a0a` | Warning text |
| `--warn-pale` | `#fdf2e3` | Warning row backgrounds |

### Typography

- **Serif (display):** DM Serif Display. Used for `h1`, `h2`, hero stats, demo screen titles. Italic spans inside the H1 (and other headings where helpful) highlight the key phrase in the signature colour.
- **Sans (body):** Instrument Sans, weights 400, 500, 600. Default font for everything else.
- **Mono:** DM Mono, weights 400 and 500. For file names, dates, fee-earner codes, URLs, anywhere that should read as data.

Stat-number sizing inside the hero stats bar is `2rem` serif in the signature colour, with the label below in 12px `--ink-light`.

### Layout tokens

- `--radius`: 10px (buttons, small cards, form inputs)
- `--radius-lg`: 16px (large cards, app frames, the stats bar)
- Section padding: `5rem 2rem`
- Max content width: `1100px`
- Fixed nav: 60px tall, `rgba(250,249,247,0.92)` with `backdrop-filter: blur(12px)`

### Buttons

- **Primary:** signature colour background, white text, 10px radius, no shadow. Hover darkens to `--accent-light`, lifts 1px.
- **Secondary:** transparent, `--ink` text, 1.5px `--paper-mid` border. Hover tightens the border to `--ink-light`.
- **Dark-section primary:** white background, `--ink` text. Hover goes to `--paper-warm`.

No pill buttons except small status tags. No gradients. No drop shadows.

### Cards

White (`#fff`) background, 1px `--paper-mid` border, 16px radius. No shadows.

### Section pattern

```
<div class="section-label">Three to five words</div>
<h2 class="section-title">Serif headline, sometimes with an <em>italic accent span.</em></h2>
<p class="section-sub">Optional subhead, ink-mid, max 720px.</p>
```

The section label is 12px, 600 weight, ink-light, uppercase, 0.1em letter-spacing.

---

## 3. Per-tool signature colour

Each Nimble Tech tool gets its own dark accent. It is used for:

- Nav logo mark background
- Primary CTAs
- Italic emphasis spans inside serif headings
- Section-label dots and badges
- Stat numbers inside white containers
- Demo and security section backgrounds
- Form focus borders, focus rings
- "After" or "with-tool" treatment in before/after grids

Each tool also has a `light`, `pale`, and `border` companion shade.

### Current tools

| Tool | Accent | Accent-light | Accent-pale | Accent-border |
|---|---|---|---|---|
| BundleRight | `#1c3a2e` (forest green) | `#2d5c45` | `#e8f0eb` | `#c2d9cb` |
| FixMyTime | `#2e1b4e` (indigo plum) | `#4a3275` | `#ece5f3` | `#c8bcd9` |

### Picking a new tool colour

1. Dark enough to carry white text at AAA contrast.
2. Stay in the deep, muted family. No neon, no pastel, no primary blues that look like a generic SaaS app.
3. Hue distinct from every existing tool.
4. Derive three companions: `light` (about 30% lighter, hover state), `pale` (very light tint of the same hue, for badge backgrounds), `border` (a low-saturation tint, sits between paper-mid and the pale).

A useful reference list of unused hue families: deep teal, navy, burgundy, slate, espresso, oxblood, charcoal-violet, hunter green (darker than BundleRight).

---

## 4. Page anatomy

A standard Nimble Tech one-page site, in order:

1. **Nav.** Logo mark (signature colour, 30px square, 2-3 letter monogram in mono) + product name + "by Nimble Tech" link + section links + CTA button.
2. **Hero.** Badge (pale background, signature colour text) + serif H1 with one italic accent span + sub copy + two CTAs + stats bar.
3. **Problem.** Section label + serif H2 + sub + side-by-side "Without / With" grid. Without column uses a soft red header; With column uses the signature-pale header.
4. **Demo.** Section background in signature colour. Inside, a paper-coloured app frame with browser chrome (mac-style dots + URL bar). Stepped walkthrough with step pips and panels, or a single deep-dive review screen.
5. **How it works.** Section background `--paper-warm`. Four steps with serif numerals in signature-colour circles.
6. **Security.** Section background in signature colour. Three-column card grid (white cards, ink text) with 6 cards covering: AI safety, encryption, infrastructure region, data lifecycle, minimal data model, defence in depth.
7. **Pricing.** Nimble Pass explainer block + two-card grid (free trial + featured pay-as-you-go). See §5.
8. **CTA.** Dark (`--ink`) background, serif H2 over two lines, single primary button. Italic accent span optional. Two-line punch-line pattern is the default (e.g. "Stop spending hours on bundling. / Start spending them on the law.").
9. **Waitlist.** White form on paper background. Three fields: full name, email, optional beta-tester checkbox. **No firm field.** Netlify-compatible (`data-netlify="true" action="/success"`). Submit button has a sibling empty `.form-message` div for inline success/error states.
10. **Footer.** Dark ink, centred, three lines: "X is a product of Nimble Tech · Privacy · Terms · Sub-processors · Contact", then copyright, then Companies House registration.

---

## 5. Nimble Pass pricing model

Every Nimble Tech tool draws from the same credit pool. Pricing copy on every tool's page must reflect this.

- Section H2: `"The Nimble Pass.<br>One wallet, every Nimble tool."` (constant across every tool).
- Section sub-line leads with: "A single set of credits that works across every product we build." Then a tool-specific aspirational example of cross-product spend, e.g. "Top up once, then use the same balance to verify a document in VerifyDoc today and create a bundle in BundleRight tomorrow."
- The three-tile explainer ("What that means") is fixed by structure and largely fixed by wording:
  - Tile 1, "Buy credits when you need them" — "No subscription, no monthly fee. If you only use a tool twice a year, you only pay for those two times. Credits stay valid for 12 months from your last top-up."
  - Tile 2, "Spend them anywhere in the family" — "Today that means BundleRight. Tomorrow it'll mean more, and your credits will already work there. Share your key with anyone at the firm." A tool may also use this tile to surface a tool-specific Nimble Pass behaviour (e.g. VerifyDoc swaps in "Unchanged statements cost nothing" as a third differentiator).
  - Tile 3, "Accessible to any firm" — "The same quality of software, without the lock-in or the IT rollout. Pay only for what you use, and start in minutes."
- The "today that means" line names only currently-live products. As products launch, this line is updated across every tool site.
- Free-trial card frames the trial in tool-specific terms ("Try one bundle on us", "Verify part of a document on us") with "no card required" in the body.
- Featured pay-as-you-go card displays "Pricing coming soon" as the headline rate until per-credit pricing is set, with a one-paragraph explanation and a footer line "∞ products supported. Today BundleRight, tomorrow more." (updated as products launch).
- Avoid per-unit pricing on individual tool pages. Unit pricing varies per tool and can change.

---

## 6. Demo section

Every tool's demo lives inside a paper-coloured "app" frame with mac-style traffic-light dots and a fake URL bar showing `app.<tool>.com / matters / <sample-matter>`.

Inside the frame, two patterns are valid:

- **Stepped walkthrough.** Step pips (mono numerals in circles) with a horizontal line between them. Active pip is signature-colour fill, done pips use signature-pale fill, untouched pips are white with paper-mid border. Each step has its own panel. Reusable across tools.
- **Single review screen.** One full-width interactive view. Used when the product's value is best shown in one screen rather than a sequence.

For FixMyTime specifically, the demo uses a single review screen with four colour-coded row states: soft green (chargeable, no issues), soft amber (chargeable, with issues), soft red (non-chargeable), soft blue (added by FixMyTime). See `FixMyTime/index.html` for the working implementation.

---

## 7. Security section content

A consistent six-card grid across every tool. Card titles are stable, body copy is tool-specific.

1. AI through AWS Bedrock (no retention, no logging, no training)
2. Encrypted in transit and at rest (TLS, customer-managed KMS, Secrets Manager)
3. Infrastructure region (UK, eu-west-2, private VPC for Bedrock)
4. Data lifecycle (session-scoped, deletion on close)
5. Minimal data model (licence key, firm name, billing email)
6. Defence in depth (WAF, rate limits, read-only filesystem, MFA, no long-lived keys)

If the tool has a specific exception, swap card 4 or 5 to reflect it. The titles and order should otherwise stay constant.

---

## 8. Footer pattern

Identical across every Nimble Tech site:

```
X is a product of Nimble Tech  ·  Privacy policy  ·  Terms  ·  Sub-processors  ·  Contact
© <year> Nimble Tech Ltd. All rights reserved.
Nimble Tech Ltd is registered in England and Wales (company no. 16203504).
```

Three lines, decreasing opacity. Privacy, terms, sub-processors, and contact link to `/privacy.html`, `/terms.html`, `/sub-processors.html`, `/contact.html` at the tool's domain.

---

## 9. Subpage pattern

Every Nimble Tech tool site has five subpages: `privacy.html`, `terms.html`, `sub-processors.html`, `contact.html`, and `success.html`. The first four are linked from the footer of the one-pager; `success.html` is the Netlify form-submission landing page used by the waitlist form on the one-pager and the contact form on `contact.html`.

The standing pattern is the BundleRight implementation (`~/projects/BundleRight Website/`). New tool sites fork those files verbatim, swap product name, signature colour, monogram, and the product-specific paragraphs, and ship. The shape, components, and section structure stay constant.

### Layout, all five subpages

- Same fixed nav as the one-pager. Logo, product name, "by Nimble Tech", and the three section links (`index.html#how`, `index.html#security`, `index.html#pricing`) all stay. There is **no** "Back to site" button. The right-hand CTA from the one-pager drops off.
- Content sits in a `<div class="content">` wrapper, max-width 800px for privacy and terms, 900px for sub-processors, 700px for contact and success. Padding `120px 2rem 80px`.
- Page header: serif `h1`, plain, **no italic accent span**, `clamp(2rem, 5vw, 2.8rem)`. Below it, a plain `<p class="last-updated">Last updated: <date></p>` at 14px, `--ink-light`. No section label, no mono caption.
- Body: serif `h2` at 1.5rem with `margin-top: 2.5rem; margin-bottom: 1rem`. Body `p` and `li` at 15px, `--ink-mid`, line-height 1.7. `ul`/`ol` indented `margin-left: 1.5rem`.
- Links: `--accent` colour, no underline by default, underline on hover.
- Same footer as the one-pager. The footer is rendered identically on every subpage; subpages do not mark the current page as active.

### Title format

Browser `<title>` is `"<ProductName>, <page name>"` with a comma separator. No em dashes. Example: `VerifyDoc, privacy policy`.

### Tone

Plain English first, lawyer second. A partner skimming any of the four legal pages should find no surprises. Each page opens with a one-paragraph summary of what the page is and who it binds.

### Privacy policy structure (12 sections)

H2 headings in order:
1. Information We Collect
2. How We Use Your Information
3. Zero Data Retention (ZDR)
4. Data Storage and Security
5. Data Sharing
6. Your Rights
7. Data Retention
8. Cookies, Browser Storage, and Tracking
9. International Transfers
10. Children's Privacy
11. Changes to This Policy
12. Contact Us

Sections 1, 5, 7 are itemised by category (waitlist data, account and billing data, document/processing data, security logs, etc.) with `<strong>` lead-ins. Section 3 carries the load on the AI architecture: AWS Bedrock under the AWS DPA, no retention, no training use, no direct Claude API path, automated regression test that fails the build if a future change tries to bypass Bedrock.

### Terms structure (20 sections)

H2 headings in order:
1. Who We Are
2. The Service
3. Who Can Use \<Tool\>
4. Licence Keys and Access
5. Credits, Pricing, and Payment
6. Refunds
7. Acceptable Use
8. Your Data and Privacy
9. Data Protection Roles
10. Confidentiality
11. Intellectual Property
12. Service Availability
13. Warranties and Disclaimers
14. Limitation of Liability
15. Indemnity
16. Suspension and Termination
17. Changes to These Terms
18. Governing Law and Jurisdiction
19. Miscellaneous
20. Contact

Section 13 must explicitly require professional review before the tool's output is used in a formal legal context. Section 14 caps liability at the greater of (a) credits paid in the preceding 12 months or (b) £100. Section 18 fixes governing law as England and Wales.

### Sub-processors structure

- One-paragraph preamble.
- A callout box (background `--accent-pale`, left border `--accent`) summarising the AI architecture: AWS Bedrock under the AWS DPA, no retention, no training use.
- One H2 "Current sub-processors" above a single table with columns: **Sub-processor**, **Purpose**, **Data**, **Region**.
- Eight standing rows, in this order: AWS (hosting + storage), AWS Bedrock (Sonnet for the core AI operation), AWS Bedrock (Haiku for OCR), Stripe, Amazon SES, Netlify, Google Fonts (Google Ireland Limited), Cloudflare.
- Two further H2 sections: "Changes to this list" and "How we choose and oversee sub-processors". Final H2 "Contact" links to the contact form.

### Contact structure

- Centred H1 "Get in touch" and a centred subtitle paragraph.
- A single contact form (`<form name="contact" method="POST" data-netlify="true" action="/success">`) inside a `.contact-form` card. Fields: full name, email, firm name (optional), subject, message. Single submit button "Send message".
- Underneath the form, a horizontal rule and a small "Registered office" block with the company name, registered office address, and Companies House number.

### Success structure

- Centred H1 "Success." and a one-line subtitle "We'll be in touch." (Use a full stop, not an exclamation mark, in line with §1.)
- No body content. Nav and footer identical to the other subpages.

### Domain-specific values to swap

Per tool, when forking from BundleRight:

- Product name, monogram (`BR` → e.g. `VeD`), and product domain (`bundleright.co.uk` → e.g. `verifydoc.co.uk`).
- Signature colour and companions (`--accent`, `--accent-light`, `--accent-pale`).
- Workflow-specific copy: BundleRight talks about "documents", "bundles", "General Bundle", "SENDIST Bundle". The fork swaps these for the new tool's primary noun (`statements`, `verification schedules`, etc.) and workflow names.
- Free-trial allowance in terms §5 ("25 documents" → e.g. "50 statements").
- Email addresses on the contact and privacy pages (`privacy@bundleright.co.uk` → `privacy@<tool>.co.uk`).

Everything else, including the registered office address (167-169 Great Portland Street, 5th Floor, London, England, W1W 5PF), company number (16203504), and the AWS Bedrock / ZDR architectural claims, stays identical across all tools.

---

## 10. Working references

- **BundleRight (canonical):** `~/projects/BundleRight Website/index.html` and the four subpages alongside it. BundleRight is the standing reference for both the one-pager and the subpage pattern. When the brand guide and BundleRight disagree, the guide is updated to match BundleRight (or the disagreement is flagged here).
- **VerifyDoc (deep teal):** `~/Documents/Claude/Projects/NimbleTech/Tools/VerifyDoc/docs/`. Implementation of the same pattern with the deep-teal accent and the verification-schedule demo.
- **FixMyTime (indigo plum):** `~/Documents/Claude/Projects/NimbleTech/Tools/FixMyTime/docs/index.html`. Earlier implementation; behind BundleRight on a few details (firm field in waitlist, smaller stat-num). Will be brought into line when next touched.
- **FixMyTime product brand (for the app UI, not the website):** `FixMyTime_Brand_Guidelines.md` in the FixMyTime project knowledge.

When building a new Nimble Tech tool site, start by copying the BundleRight `index.html` and its four subpages, then swap the four `--accent*` variables to the new tool's signature palette, swap the monogram and product domain, update the copy and the demo content, and confirm the cross-product references in the Nimble Pass section reflect the products that are live at launch.
