# Product

## Register

product

## Users

Thai everyday shoppers and budget-trackers, primarily on mobile. Two contexts: (1) quick in-store check at checkout — rushed, one-handed, need the number fast; (2) deliberate daily/monthly tracking — reviewing remaining allowance, planning spend for the week. Both speak Thai natively. Familiarity with เป๋าตัง and PromptPay is the baseline mental model for what a trustworthy financial app feels like.

## Product Purpose

A personal subsidy calculator and tracker for the Thai government ไทยช่วยไทยพลัส 60/40 co-payment program (Jun–Sep 2569). Enter purchase amount, see instantly how much the government pays vs. how much you pay, record it, and track remaining daily / monthly / campaign allowance. All data stays on-device. No server, no account. Works fully offline, installable as a PWA.

## Brand Personality

Friendly, Simple, Helpful. The emotional goal: feels like a knowledgeable friend who explains your money clearly — not a government portal, not a startup. Warm confidence. The interface answers "am I okay?" before the user has to ask.

## Anti-references

- Overly playful or cartoon-heavy aesthetics — too casual for a tool that tracks money.
- Western fintech gloss — frosted glass, abstract gradients, heavy dark mode drama. Ignores Thai mobile context.
- Thai government portal density — bureaucratic layout, walls of text, formal coldness.
- Generic SaaS dashboard patterns — sidebar nav, hero metric cards, gradient text.

## Design Principles

1. **Answer the question before it's asked.** The primary number (how much gov pays, how much left today) must land in under one second of glance time. Nothing should require reading first.
2. **Thai by design.** Language, numerals, date formatting, color associations — culturally rooted, not translated. The app should feel made for Thai users, not localized for them.
3. **Trust through precision.** Friendly tone does not mean imprecise. Every baht shown must be correct and explained. Uncertainty is shown as a note, never hidden.
4. **Progressive depth.** The quick-check path (enter amount → see split → confirm) must be zero-friction. History, capacity view, pacing warnings are available but never in the way.
5. **Device-native, not web-native.** Tap targets, safe areas, font choices, spacing — should feel like an app installed on a Thai phone, not a webpage.

## Accessibility & Inclusion

WCAG AA minimum: contrast ratios, adequate tap target sizes (≥44px), visible focus states. Existing `prefers-reduced-motion` support must be preserved in all design work.
