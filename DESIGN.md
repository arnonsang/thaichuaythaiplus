---
name: ไทยช่วยไทยพลัส
description: Thai government 60/40 subsidy calculator and personal spending tracker
colors:
  thai-green: "#1a7f5a"
  thai-green-deep: "#0f5e41"
  thai-green-bright: "#2bb37e"
  trust-blue: "#2563eb"
  page-mist: "#f3f6f4"
  surface-white: "#ffffff"
  ink-forest: "#13241d"
  muted-sage: "#576a5e"
  divider-dew: "#e3ebe6"
  amber-warning: "#b45309"
  warning-cream: "#fff7ed"
  danger-ember: "#c2410c"
  danger-blush: "#fef2f2"
typography:
  display:
    fontFamily: "'Sukhumvit Set', 'IBM Plex Sans Thai', 'Noto Sans Thai', system-ui, sans-serif"
    fontSize: "2rem"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "normal"
  headline:
    fontFamily: "'Sukhumvit Set', 'IBM Plex Sans Thai', 'Noto Sans Thai', system-ui, sans-serif"
    fontSize: "1.18rem"
    fontWeight: 800
    lineHeight: 1.3
    letterSpacing: "-0.2px"
  title:
    fontFamily: "'Sukhumvit Set', 'IBM Plex Sans Thai', 'Noto Sans Thai', system-ui, sans-serif"
    fontSize: "0.95rem"
    fontWeight: 800
    lineHeight: 1.4
  body:
    fontFamily: "'Sukhumvit Set', 'IBM Plex Sans Thai', 'Noto Sans Thai', system-ui, sans-serif"
    fontSize: "0.87rem"
    fontWeight: 600
    lineHeight: 1.5
  label:
    fontFamily: "'Sukhumvit Set', 'IBM Plex Sans Thai', 'Noto Sans Thai', system-ui, sans-serif"
    fontSize: "0.79rem"
    fontWeight: 700
    lineHeight: 1.4
rounded:
  xs: "9px"
  sm: "12px"
  md: "14px"
  lg: "18px"
  full: "999px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "16px"
  lg: "24px"
components:
  button-primary:
    backgroundColor: "{colors.thai-green}"
    textColor: "{colors.surface-white}"
    rounded: "{rounded.md}"
    padding: "16px"
  button-primary-hover:
    backgroundColor: "{colors.thai-green-deep}"
    textColor: "{colors.surface-white}"
    rounded: "{rounded.md}"
    padding: "16px"
  chip-default:
    backgroundColor: "{colors.surface-white}"
    textColor: "{colors.ink-forest}"
    rounded: "{rounded.sm}"
    padding: "10px 8px"
  chip-full:
    backgroundColor: "#f0faf5"
    textColor: "{colors.thai-green-deep}"
    rounded: "{rounded.sm}"
    padding: "10px 8px"
  card:
    backgroundColor: "{colors.surface-white}"
    rounded: "{rounded.lg}"
    padding: "18px 16px"
  input-amount:
    backgroundColor: "#fbfdfc"
    textColor: "{colors.ink-forest}"
    rounded: "{rounded.md}"
    padding: "14px 16px 14px 42px"
  badge-gov:
    backgroundColor: "#e8f5ee"
    textColor: "{colors.thai-green-deep}"
    rounded: "{rounded.full}"
    padding: "6px 11px"
  badge-month:
    backgroundColor: "#eef2ff"
    textColor: "#3730a3"
    rounded: "{rounded.full}"
    padding: "6px 11px"
  result-box-gov:
    backgroundColor: "#e9f7ef"
    textColor: "{colors.thai-green-deep}"
    rounded: "{rounded.sm}"
    padding: "14px"
  result-box-user:
    backgroundColor: "#eaf0ff"
    textColor: "#1e40af"
    rounded: "{rounded.sm}"
    padding: "14px"
  button-ghost-danger:
    backgroundColor: "{colors.surface-white}"
    textColor: "{colors.danger-ember}"
    rounded: "{rounded.sm}"
    padding: "12px"
---

# Design System: ไทยช่วยไทยพลัส

## 1. Overview

**Creative North Star: "The Pocket Cashier"**

This system is built for a specific moment: phone in one hand, items on the counter, needing one number fast. The design eliminates everything between the user's question ("how much do I actually pay?") and the answer. Warmth comes from color, not decoration. Precision comes from typography, not density.

The palette speaks in two voices: Thai Green holds government money (confidence, civic trust, the reassuring green of official approval), Trust Blue holds the user's own contribution (personal, actionable, distinct). Neither voice competes. Neutral surfaces — the barely-there Page Mist background, clean white cards — recede completely so numbers read first.

This system explicitly rejects the bureaucratic density of Thai government portals, the cartoon casualness that would undermine financial trust, and the generic Western fintech gloss of frosted cards and abstract gradients. It is a Thai tool, used by Thai people, on Thai phones. Every decision reflects that context: the font stack, the color associations, the compact vertical rhythm suited to a narrow mobile screen.

**Key Characteristics:**
- Number-first hierarchy: monetary values always read at headline scale, labels recede
- Two-voice semantic color: green = government benefit, blue = user's cost; never decorative
- Thai-native font stack, no Latin primary; legible at 0.78rem on older phones
- Broadly rounded containers (18px cards) that feel native to mobile, not web-ported
- Single-layer shadow vocabulary: cards float off the background, everything else stays flat
- Full prefers-reduced-motion support throughout; animation is an enhancement, not a requirement

## 2. Colors: The Two-Voice Palette

The palette is semantically split, not aesthetically decorative. Thai Green owns all government-side data. Trust Blue owns all user-side data. Neutrals provide structure without competing.

### Primary
- **Thai Green** (`#1a7f5a` / oklch(52.5% 0.115 162)): The government subsidy color. Appears on the primary CTA button, progress meter fills, logo background, gov result box tint, and all gov data text. Never used decoratively. Every green element means "this is your benefit from the government."
- **Thai Green Deep** (`#0f5e41` / oklch(38.5% 0.085 162)): Dark variant of Thai Green. Used for text on green-tinted surfaces — badge labels, result box values, links. Provides WCAG AA contrast on light green backgrounds.
- **Thai Green Bright** (`#2bb37e` / oklch(65% 0.13 162)): The lighter gradient stop. Used as the starting point in progress bar fills and the button gradient. Not used standalone; always part of a directional gradient.

### Secondary
- **Trust Blue** (`#2563eb` / oklch(52% 0.245 265)): The user's contribution color. Appears on user result box background and text, user-side history split labels, and the month badge. Every blue element means "this is what comes out of your pocket."

### Neutral
- **Page Mist** (`#f3f6f4` / oklch(96.5% 0.008 162)): The app background. A barely-perceptible green tint keeps the surface harmonized with Thai Green without drawing attention. This is what the app sits on.
- **Surface White** (`#ffffff`): Card and input backgrounds. Pure white creates the clearest contrast against Page Mist to delineate card boundaries. Future new surfaces should use a tinted near-white instead.
- **Ink Forest** (`#13241d` / oklch(16% 0.028 165)): Primary text color. Near-black with a deep green undertone, not neutral charcoal. The system's darkest surface; used for all primary labels, headings, and values.
- **Muted Sage** (`#576a5e` / oklch(44% 0.018 165)): Secondary text, labels, timestamps, meter annotations, placeholder text. WCAG AA compliant against both Page Mist (5.2:1) and white cards (5.6:1). Recedes without disappearing.
- **Divider Dew** (`#e3ebe6` / oklch(92.5% 0.012 162)): Borders, separators, meter track backgrounds, input stroke at rest. Barely visible against white; its job is structure, not presence.
- **Amber Warning** (`#b45309` / oklch(51% 0.135 54)): Subsidy cap warning state only. Appears on the cap-exceeded note and pacing callout. No decorative use.
- **Warning Cream** (`#fff7ed` / oklch(98% 0.022 73)): Warning background. Pairs exclusively with Amber Warning text.
- **Danger Ember** (`#c2410c` / oklch(52% 0.175 34)): Delete actions, campaign-ended state, critical pacing alert. The sharpest, most attention-demanding color in the system.
- **Danger Blush** (`#fef2f2` / oklch(97.5% 0.012 16)): Danger background. Pairs exclusively with Danger Ember text.

### Named Rules
**The Two-Voice Rule.** Green = government money. Blue = your money. No element switches voices. If a number is green, it belongs to the subsidy. If it is blue, it comes out of your pocket. This semantic contract cannot be violated without confusing the user about who is paying what.

**The Semantic-Only Rule.** Color in this system communicates meaning, not mood. No green gradients on neutral UI elements, no blue accents on non-user content. If the color has no semantic reason to be there, it should not be there.

## 3. Typography

**Primary Font:** "Sukhumvit Set" (with "IBM Plex Sans Thai", "Noto Sans Thai", system-ui, -apple-system, "Segoe UI" as progressive fallbacks)

**Character:** A Thai-native sans-serif stack. Sukhumvit Set is designed specifically for Thai script with excellent legibility at small sizes. The fallback chain ensures readability on older Android devices and phones without the premium Thai font installed. No Latin-primary font appears anywhere in this stack; the app reads Thai first, always.

### Hierarchy
- **Display** (800 weight, 2rem, line-height 1.1): Reserved for the amount input field only. The biggest typographic element on screen; the number you are entering to calculate your payment.
- **Result Values** (800 weight, 1.7rem, line-height 1.1): Gov-pays and user-pays output values in the split result boxes. Immediately readable after input, displayed side-by-side for instant comparison.
- **Headline** (800 weight, 1.18rem, line-height 1.3, -0.2px letter-spacing): Page title only (ไทยช่วยไทยพลัส). Single use across the entire app.
- **Title** (800 weight, 0.95rem, line-height 1.4): Section card headings (h2). All hierarchy is from weight contrast; no size inflation between titles.
- **Body** (600 weight, 0.86-0.9rem, line-height 1.5): Primary content text, hints, descriptions, and callout messages. Contained within the 520px max-width layout.
- **Label** (600-700 weight, 0.78-0.82rem, line-height 1.4): Timestamps, badge text, meter annotations, small helper copy. Default color is Muted Sage.

### Named Rules
**The Weight-First Rule.** Hierarchy is established through font weight (800 vs. 700 vs. 600), not through size variance. Most of the UI sits between 0.78rem and 0.95rem — a compressed range by design. Never inflate sizes to establish hierarchy; reach for weight first.

**The Number Rule.** Monetary values always appear at a larger size and heavier weight than their associated label. The value is the answer. The label is context. If they look the same size, the hierarchy is broken.

## 4. Elevation

This system is flat by default. Shadow marks a structural boundary, not an aesthetic choice.

One shadow exists in the vocabulary: `0 2px 14px rgba(16,60,40,.08)` — a shallow vertical offset, wide diffuse spread, at near-zero opacity with a green tint sourced from Ink Forest's hue. It lifts cards off the Page Mist background just enough to read as a contained interactive surface. No blur drama, no multiple layers, no directional key lighting.

The toast notification uses a stronger variant (`0 8px 24px rgba(0,0,0,.25)`) because it must read above any surface at any scroll position.

### Shadow Vocabulary
- **Surface lift** (`0 2px 14px rgba(16,60,40,.08)`): Applied to all card containers and the flip card. The green tinting aligns with the brand hue so the shadow feels like part of the system, not a default.
- **Overlay float** (`0 8px 24px rgba(0,0,0,.25)`): Applied to the toast notification only. Stronger, untinted, because the toast must be unmistakably above everything else.

### Named Rules
**The Flat-By-Default Rule.** Every surface starts flat. Shadow is applied exactly where a card boundary must be perceptible against the Page Mist background. Inputs, buttons, chips, badges, and result boxes are all flat. The shadow exists because cards need it; not as an ambient atmosphere or a style statement.

## 5. Components

### Pay Button (Primary CTA)
The most important tap target in the app. Full-width, broadly rounded (14px), solid Thai Green fill. Warm and direct.
- **Shape:** Broadly rounded corners (14px)
- **Primary:** Linear gradient from Thai Green (#1a7f5a) to #23a373, white text, full width, 16px vertical padding, 800 weight
- **Resting shadow:** `0 6px 16px rgba(26,127,90,.28)` — a green glow that reinforces the brand color at rest
- **Active/press:** Vertical shift down 1px (`translateY(1px)`), shadow compresses
- **Disabled:** Flat grey (#c2cdc7), no shadow, not-allowed cursor
- **Focus-visible:** 2px Thai Green outline, 3px offset

### Quick Amount Chips
A horizontal row of shortcut amounts. Compact but comfortable to tap (min 44px height).
- **Default:** White background, Ink Forest text, 1.5px Divider Dew border, 12px radius
- **Full-day variant:** Light green tint (#f0faf5), Thai Green Deep text, green-tinted border (#cfe9dc). Visually distinguished from the plain chips — this chip is the recommended action.
- **Active/press:** Scale 0.97 (`transform: scale(.97)`)
- **Disabled:** 40% opacity, not-allowed cursor
- **Focus-visible:** 2px Thai Green outline, 2px offset

### Section Cards
The primary container unit. All major content sections live in cards.
- **Corner Style:** Broadly rounded (18px), the softest curve in the system
- **Background:** Surface White (#ffffff)
- **Shadow:** Surface-lift shadow (the only use outside the toast)
- **Border:** None
- **Internal Padding:** 18px vertical, 16px horizontal

### Amount Input
The single most important interactive element. Oversized, designed for rapid numeric entry, one-handed.
- **Style:** 2px Divider Dew border at rest, 14px radius, near-white background (#fbfdfc)
- **Focus:** Border shifts to Thai Green, 0.15s transition. No glow or shadow — border shift only.
- **Typography:** Display scale (2rem, 800 weight), Thai-first font stack
- **Baht symbol:** Absolutely positioned 16px from left, Muted Sage color, 1.6rem — present but not competing with the input value

### Result Split Boxes
Side-by-side panels showing the gov-pays / user-pays breakdown. The semantic color contract made visible.
- **Gov box:** Light green tint (#e9f7ef), Thai Green Deep text; answers "what the government gives you"
- **User box:** Light blue tint (#eaf0ff), dark blue text (#1e40af); answers "what you actually pay"
- **Shape:** 14px radius, no border, no shadow, flat
- **Value typography:** 1.7rem, weight 800 — the result, not commentary

### Status Badges
Compact pills in the header showing campaign timeline and current month.
- **Gov / campaign badge:** Light green (#e8f5ee), Thai Green Deep text, green border (#cfe9dc)
- **Month badge:** Light indigo (#eef2ff), deep indigo text (#3730a3), indigo border (#dbe1ff)
- **Shape:** Full pill (999px radius), 6px 11px padding
- **Typography:** 0.78rem, weight 700

### Progress Meters (Signature Component)
Three-tier subsidy tracker (daily / monthly / campaign). The most information-dense element in the app; the flip card reveals a complementary capacity view.
- **Track:** Light greenish grey (#eef2f0), 12px height, pill ends (999px radius)
- **Fill at >50%:** Green gradient, `linear-gradient(90deg, #2bb37e, #1a7f5a)` — healthy, positive
- **Fill at 25-50%:** Amber gradient — mid-range warning
- **Fill at 0-25%:** Orange gradient — running low
- **Fill at 0%:** Flat red (#dc2626) — exhausted
- **Shine animation:** Sweeping white highlight at 2.6s loop; disabled with `prefers-reduced-motion: reduce`
- **Number pop:** Scale-to-1.28 animation on value change; disabled with `prefers-reduced-motion: reduce`
- **Stacked variant (flip back):** Two-segment fill — green segment for gov portion, blue segment for user portion — mirroring the Two-Voice color contract

### History Rows
Compact transaction log, grouped by date.
- **Layout:** Flex row with fixed-width time (46px), amount (74px), flex-1 split annotation, and fixed delete button
- **Dividers:** 1px solid light grey (#f1f5f3) between rows, none after the last row
- **Split text:** Gov portion in Thai Green Deep; user portion in dark blue (#1e40af)
- **Delete button:** Danger Blush background, Danger Ember text, 9px radius, 7px 11px padding

### Toast Notification
Ephemeral confirmation for pay and delete actions. Always bottom-center.
- **Background:** Ink Forest (#13241d) — the darkest surface in the system; unmistakable
- **Shape:** Full pill (999px radius)
- **Motion:** Slides up 20px and fades in, 0.25s; reverses on dismiss. `cubic-bezier` default easing.
- **Position:** Fixed, bottom 24px, centered horizontally

## 6. Do's and Don'ts

### Do:
- **Do** use Thai Green exclusively for government subsidy data: gov amounts, gov result boxes, progress bars, the primary CTA, and the logo.
- **Do** use Trust Blue exclusively for user-pays data: user amounts, user result boxes, history split labels.
- **Do** maintain the Thai-first font stack ("Sukhumvit Set", "IBM Plex Sans Thai", "Noto Sans Thai"). Never replace with a Latin-primary or decorative display font.
- **Do** keep card shadows at `0 2px 14px rgba(16,60,40,.08)` exactly. The green tint is intentional; a neutral grey shadow breaks the system's coherence.
- **Do** use weight 800 for all monetary values regardless of size. The number must always feel heavier than its label.
- **Do** ensure all tap targets are minimum 44px in height: buttons, chips, delete controls, and navigation elements.
- **Do** preserve every `prefers-reduced-motion` guard in the codebase. These protect users; never remove them when adding new animation.
- **Do** use 14px or 18px radius for interactive containers (inputs, buttons, cards). Tighter radii feel web-page; broader radii feel native.

### Don't:
- **Don't** use cartoon or playful aesthetics: rounded mascot illustrations, bright emoji-heavy layouts, oversized icon characters. This app tracks real money and must earn financial trust.
- **Don't** apply Western fintech gloss: frosted glass (`backdrop-filter: blur`), abstract layered gradients, heavy dark-mode drama, glassmorphism as default. The app is used outdoors on a phone in ambient daylight.
- **Don't** reproduce Thai government portal density: walls of regulatory text, multi-column bureaucratic layouts, formal header bars with official crests or seals.
- **Don't** use generic SaaS dashboard patterns: sidebar navigation, hero metric card templates (big number, small label, gradient accent), identical card grids, gradient text (`background-clip: text`).
- **Don't** use `border-left` or `border-right` greater than 1px as a colored accent stripe on cards, list items, or callouts. Use background tints, full borders, or nothing.
- **Don't** switch color semantics. A blue element cannot represent government data. A green element cannot represent the user's personal cost. The Two-Voice Rule is not optional.
- **Don't** add shadow depth beyond the defined vocabulary. No blur-heavy multi-layer shadows, no `box-shadow` stacking, no hover shadows on flat elements. Flat-By-Default Rule applies.
- **Don't** create new surfaces using pure `#fff` without the Page Mist context. New additions should use a tinted near-white (oklch 97-99%, chroma 0.005-0.01 at hue 162) to stay harmonized with the background.
- **Don't** shrink monetary values below Title scale (0.95rem / 800 weight) regardless of space constraints. If space is tight, reduce the label, not the number.
