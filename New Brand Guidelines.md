# Nimble Tech Website Brand Guidelines — New

For all public-facing websites under the Nimble Tech header. Currently: Nimble Tech parent site, BundleRight, FixMyTime; VerifyDoc to follow. Future tools follow the same system, with their own signature colour and tonal palette.

This document covers websites only. Product UI (the apps themselves) may use a different visual treatment, defined in each product's own brand guide.

**Supersedes** `Nimble Tech Website Brand Guidelines.md` for any site that adopts this system. The old guide remains in the repo for reference; sites still on it (per `index.html` etc.) continue to work, but new builds and refreshes use this one.

**Canonical implementation:** `explorations/take-4-tonal-navy.html`.

---

## 1. Audience and voice

Unchanged from the previous guide. UK law firms and adjacent professional services. Decision-makers and the fee-earners who use the tools day to day.

Voice is calm, precise, unboastful. Short, declarative sentences. Address real objections (lock-in, security, change cost) rather than pretend they do not exist.

Rules, no exceptions:

- No exclamation marks.
- Commas over dashes for rhythm. No em dashes anywhere.
- No buzzwords: no "revolutionary", "seamless", "leverage", "synergy", "cutting-edge", "transform".
- Lawyers are spoken to as equals.

---

## 2. What's changed from the old system

The old guide leaned literary-editorial: a warm cream paper background, DM Serif Display headlines, an italic accent span on the H1 carrying the key phrase. That treatment had become indistinguishable from a class of AI-product marketing sites — most visibly Claude.ai. The new system keeps the **logos** and the **per-tool signature colours**, and replaces:

- Cream paper background → a pale tonal tint of each tool's own signature colour.
- DM Serif Display headlines → Geist, used at heavy display weights for the H1.
- Italic serif accent span → a solid signature-colour word at heavier weight (no italic).
- The "Building in public" hero badge → removed. The hero leads with the H1.

Everything else — the structural anatomy of the one-pager, the Nimble Pass pricing model, the security card grid, the subpage pattern — carries over.

---

## 3. Shared visual system

Every Nimble Tech website inherits this base. The only thing that changes per tool is the signature colour and its derived tonal palette (see §4).

### Tonal background palette (Nimble Tech parent)

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#eef2f8` | Page background, pale navy tint |
| `--bg-deep` | `#d2dcea` | Deeper navy band, used for the mission section |
| `--bg-card` | `#ffffff` | White cards on the tinted ground |
| `--line` | `#b8c5d8` | Section dividers, nav border, card borders |
| `--line-soft` | `#d0dae8` | Internal hairlines inside cards |
| `--ink` | `#0f1a2e` | Primary text |
| `--ink-mid` | `#4a5670` | Body text |
| `--ink-light` | `#8b94a8` | Captions, labels, mono small text |

Per-tool tonal palettes derive from the signature colour. See §4.

### Typography

- **Sans (everything):** Geist, weights 400, 500, 600, 700, 800. Used for nav, headings, body, buttons, form fields. Loaded from Google Fonts (`Geist`).
- **Mono:** Geist Mono, weights 400 and 500. Used for nav monogram marks, section labels where data-flavoured, stat labels, pricing rows, footer.
- **No serif.** Anywhere.

H1 uses Geist at weight 700, `font-size: clamp(2.8rem, 6.5vw, 5rem)`, `line-height: 1.0`, `letter-spacing: -0.035em`. The accent word inside the H1 uses the signature colour with weight bumped to 800 — that one-step weight shift carries the emphasis the italic used to.

Sub-copy uses Geist weight 400 at `1.15rem`, `line-height: 1.55`, colour `--ink-mid`.

### Layout tokens

- `--radius`: 10px (cards, form inputs)
- `--radius-lg`: 18px (large cards, the Nimble Pass card, mission cards)
- Buttons are pill-shaped (`border-radius: 999px`), not 10px corners.
- Section padding: `6rem 1.5rem`
- Max content width: `940px`
- Fixed nav: 64px tall

### Nav

- Nav background `rgba(255,255,255,0.85)` with `backdrop-filter: blur(14px)`. Sits as a white surface above the tinted page so the boundary between nav and hero reads clearly.
- Border-bottom `1px solid var(--line)` plus `box-shadow: 0 1px 0 rgba(15,26,46,0.03)` for soft elevation.
- Monogram mark: 30×30, `border-radius: 8px`, filled with `--accent`, white mono letters at 11px / weight 500.
- Product wordmark: Geist, 15px, weight 700, `letter-spacing: -0.015em`, colour `--ink`. Inherits sans from body — no explicit override needed.
- Tool sites add `by <a>Nimble Tech</a>` in Geist Mono 11px next to the wordmark. The parent Nimble Tech site does not.
- Nav links: 14px, weight 500, colour `--ink-mid`, hover `--ink`.
- Nav CTA: pill button, `--accent` background, white text, 13px / weight 600.

### Buttons

- **Primary:** signature colour background, white text, pill (`border-radius: 999px`), `padding: 13px 26px`, weight 600, 1px box-shadow underneath in the deep accent. Hover lifts 1px and shifts to `--accent-light`.
- **Secondary:** white background, `--ink` text, 1px `--line` border, same pill shape. Hover borders to `--accent`.

No drop shadows on cards. No gradients except the Nimble Pass visual and the watch-this-space band.

### Cards

White (`#fff`) background, 1px `--line-soft` border, 18px radius. Mission cards lift 2px on hover. Product rows shift to `border-color: --accent` and lift 1px.

### Section pattern

```html
<div class="section-label">Three to five words</div>
<h2 class="section-title">Heading, with an <span class="accent">accent phrase.</span></h2>
<p class="section-sub">Optional subhead, ink-mid, max 620px.</p>
```

`.section-label` is a chip: `display: inline-block`, `--accent-pale` background, `--accent` text, pill, 11px / weight 600. Replaces the old uppercase ink-light label with letter-spacing.

`.section-title` uses sans at `clamp(1.85rem, 4vw, 2.75rem)`, weight 700, `line-height: 1.1`, `letter-spacing: -0.03em`. Accent span inside is weight 800 in `--accent`.

---

## 4. Per-tool signature colour and tonal palette

Each Nimble Tech tool keeps its existing dark accent. The accent appears in:

- Nav monogram mark background
- Primary CTAs, nav CTA, form submit
- Accent span inside the H1
- Section-label chip text colour (paired with `--accent-pale` background)
- Stat numerals, mission card numerals, badge text
- The Nimble Pass visual gradient (dark accent → deep accent)
- The watch-this-space dark band

What's new under this system: each tool also gets a **tonal background palette** — a very pale tint of the same hue, used for the page atmosphere, plus a slightly deeper tint for the mission section. White cards float on the tinted ground.

### Current tools

| Tool | Accent | Accent-light | Accent-deep | Accent-pale | Page bg | Section-break bg | Line |
|---|---|---|---|---|---|---|---|
| Nimble Tech | `#1a2a44` | `#2d4a78` | `#0d1626` | `#dfe6f0` | `#eef2f8` | `#d2dcea` | `#b8c5d8` |
| BundleRight | `#1c3a2e` | `#2d5c45` | `#102019` | `#d8e4dc` | `#eaf0ec` | `#dde8e0` | `#c8d6cc` |
| FixMyTime | `#2e1b4e` | `#4a3275` | `#1a0f2c` | `#ddd3e6` | `#efebf4` | `#e3dceb` | `#d0c6db` |
| VerifyDoc | `#0f4544` | `#1d6968` | `#082827` | `#d0e0df` | `#e6efef` | `#d6e3e3` | `#c0d2d1` |

Working hero/nav implementations of each: `explorations/take-4-{tool}.html`. Side-by-side: `explorations/take-4-across-tools.html`.

VerifyDoc's accent (`#0f4544`) is a starting value for the "deep teal" hue family the old guide reserved without pinning a hex. Adjust if a more specific reading emerges.

### Picking a new tool colour and palette

1. Pick the **accent** first. Dark enough to carry white text at AAA contrast, stay in the deep muted family (no neon, no pastel, no generic SaaS blue), hue distinct from every existing tool.
2. Derive **accent-light** (about 30% lighter, hover state), **accent-deep** (about 30% darker, used in CTA button shadow and gradient bottoms), **accent-pale** (very pale tint at ~85% lightness, used as the section-label chip background).
3. Derive the **tonal background**: take the same hue at ~95% lightness with low saturation. This becomes `--bg`.
4. Derive **bg-deep** at ~85% lightness for the mission section break.
5. Derive **line** at ~75% lightness for borders.

A useful reference list of unused hue families (carries over from the old guide): deep teal, navy, burgundy, slate, espresso, oxblood, charcoal-violet, hunter green.

---

## 5. Page anatomy

A standard Nimble Tech one-pager, in order:

1. **Nav.** White-tinted surface as described in §3. Logo mark + product wordmark + (tool sites only) "by Nimble Tech" + section links + pill CTA.
2. **Hero.** Plain H1 with one signature-colour accent phrase. No badge, no eyebrow chip above. Sub-copy follows the H1. Two CTAs (primary pill + secondary pill). Optional hero stats — three small white cards in a row with mono stat labels under serif-feel-sized numerals (rendered in Geist, not serif).
3. **Mission / problem.** Mission section uses `--bg-deep` band with `--line` borders top and bottom. Section label chip + section title + section sub + three white mission cards in a grid.
4. **Demo.** Same conceptual structure as the old guide (paper-coloured app frame with browser chrome and stepped walkthrough or single review screen). Frame background uses `--bg-card` (white) under this system; chrome dots stay the standard mac traffic-light colours.
5. **How it works.** Optional fourth-section band — can re-use the `--bg-deep` treatment if a second band is helpful; otherwise plain.
6. **Security.** Dark band: signature-colour background (or deep accent gradient), white text, the same six-card grid as the old guide. Card content rules unchanged.
7. **Pricing / Nimble Pass.** Unchanged in structure (see §6). Nimble Pass card is white on the tinted page; the visual chip on the right uses an `accent-light → accent → accent-deep` gradient.
8. **Watch this space.** Dark band on the accent gradient. Centred section label chip + serif-feel-sized H2 (in Geist) + quote.
9. **Contact / waitlist.** White form card on tinted page background. Three or four fields, pill submit. Netlify-compatible (`data-netlify="true" action="/success"`).
10. **Footer.** Dark `--accent-deep` band, white text at low opacity. Three lines: links · copyright · Companies House registration.

---

## 6. Nimble Pass pricing model

Unchanged. Every Nimble Tech tool draws from the same credit pool. The §5 content rules from the old guide carry over verbatim:

- Section H2: `"The Nimble Pass.<br>One wallet, every Nimble tool."`
- Sub-line leads with: "A single set of credits that works across every product we build."
- Three-tile explainer with the same wording for the three tiles.
- "Today that means" line names only currently-live products.
- Free-trial card frames the trial in tool-specific terms.
- Featured PAYG card displays "Pricing coming soon" until per-credit pricing is set.

The only thing that changes visually: tile backgrounds are white cards (`--bg-card`) on the tinted page rather than on cream paper, and the section-label is the new chip rather than the uppercase ink-light label.

---

## 7. Demo section

Conceptually unchanged from the old guide. The app frame uses `--bg-card` (white) instead of paper cream. Step pips, panel structure, single-review screen, and the FixMyTime four-state row colour-coding all carry over.

For state colours inside the demo (soft green / amber / red / blue rows), keep the tints already in use — they sit fine on a white frame.

---

## 8. Security section content

Six-card grid unchanged. Card titles stable, body copy tool-specific. Section background uses the signature colour (or the deep-accent gradient). White cards inside.

1. AI through AWS Bedrock (no retention, no logging, no training)
2. Encrypted in transit and at rest
3. Infrastructure region (UK, eu-west-2, private VPC for Bedrock)
4. Data lifecycle (session-scoped, deletion on close)
5. Minimal data model
6. Defence in depth

If the tool has a specific exception, swap card 4 or 5 to reflect it.

---

## 9. Footer pattern

Dark `--accent-deep` band, white text at low opacity. Three lines, decreasing opacity:

```
X is a product of Nimble Tech  ·  Privacy policy  ·  Terms  ·  Sub-processors  ·  Contact
© <year> Nimble Tech Ltd. All rights reserved.
Nimble Tech Ltd is registered in England and Wales (company no. 16203504).
```

Links go to `/privacy.html`, `/terms.html`, `/sub-processors.html`, `/contact.html` at the tool's domain.

---

## 10. Favicon and monogram marks

All Nimble Tech sites use a square favicon with the product monogram on the accent colour. The favicon SVG uses a mono font stack with system fallbacks so it renders consistently without depending on Geist Mono being installed:

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64">
  <rect width="64" height="64" rx="12" fill="#1a2a44"/>
  <text x="50%" y="50%" text-anchor="middle" dominant-baseline="central"
        font-family="ui-monospace, 'SF Mono', 'Geist Mono', Menlo, Consolas, monospace"
        font-size="24" font-weight="500"
        fill="#ffffff" letter-spacing="-0.5">NT</text>
</svg>
```

Per tool, swap:

- `fill` of the rect to the tool accent.
- The monogram text (`NT` → `BR`, `FMT`, `VDo`).

The 30×30 nav monogram mark inside the live site uses Geist Mono 11px / weight 500 / white on accent, same shape and proportions.

---

## 11. Subpage pattern

Structurally unchanged from the old guide (privacy, terms, sub-processors, contact, success). Each subpage uses the same nav as the one-pager. Body lives in a content wrapper at the widths the old guide specifies (800px for privacy and terms, 900px for sub-processors, 700px for contact and success).

Visual updates under this system:

- Page background is the tool's `--bg` (tonal tint), not cream.
- H1 is plain Geist 700, no italic accent span. Sizing `clamp(2rem, 5vw, 2.8rem)` stays.
- `h2` is Geist 600 at 1.5rem.
- Links use `--accent`, no underline by default, underline on hover.
- Footer identical to the one-pager.

The structure, section ordering, and content of privacy / terms / sub-processors / contact / success are all unchanged. When forking from BundleRight for a new tool site, the only things to swap remain: product name, monogram, signature colour, tonal palette, workflow-specific copy, free-trial allowance, contact email.

---

## 12. Working references

- **Nimble Tech parent (canonical):** `explorations/take-4-tonal-navy.html`. The full single-page implementation of this system.
- **Per-tool hero+nav previews:** `explorations/take-4-bundleright.html`, `take-4-fixmytime.html`, `take-4-verifydoc.html`. Each shows the system applied to that tool's tonal palette.
- **Side-by-side comparison:** `explorations/take-4-across-tools.html`. Useful when checking that the family still reads as a family.
- **Old guide:** `Nimble Tech Website Brand Guidelines.md`. Retained for reference; not active on new builds.

When building or refreshing a Nimble Tech tool site under this system, start by copying `take-4-tonal-navy.html`, swap the four `--bg*`, `--line*`, and `--accent*` variables to the tool's palette per §4, swap the favicon rect colour and monogram letters per §10, swap the nav wordmark and "by Nimble Tech" link, and swap the copy and demo content. Confirm the cross-product references in the Nimble Pass section reflect the products that are live at launch.
