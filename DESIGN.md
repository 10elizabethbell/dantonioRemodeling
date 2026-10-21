---
name: Scott J. D'Antonio Inc.
description: Light and cosmetic remodeling, inside and out. Marlton, NJ, since 1997.
colors:
  paper: "#f4f6fb"
  card: "#ffffff"
  field: "#e6ecf5"
  ink: "#142a42"
  body: "#2a3a4c"
  soft: "#4a5868"
  navy: "#23415f"
  deep: "#142a42"
  on-dark: "#f4f7fb"
  on-dark-soft: "#c9d5e3"
  brass: "#e3a83b"
  brass-2: "#edbb5c"
  brass-ink: "#835700"
  focus: "#23415f"
  error: "#b3261e"
typography:
  display:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(42px, 12vw, 80px)"
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: "-0.005em"
  headline:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(30px, 7.6vw, 48px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-0.005em"
  title:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "clamp(20px, 5.4vw, 24px)"
    fontWeight: 400
    lineHeight: 1.15
  lede:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.6vw, 19px)"
    fontWeight: 400
    lineHeight: 1.7
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: "Cal Sans, Avenir Next, Segoe UI, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.2
rounded:
  field: "10px"
  card: "24px"
  pill: "999px"
spacing:
  gutter-phone: "20px"
  gutter-desktop: "40px"
  stack: "16px"
  form-gap: "20px"
  block: "28px"
  band-phone: "64px"
  band-desktop: "96px"
components:
  button-primary:
    backgroundColor: "{colors.brass}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.brass-2}"
    textColor: "{colors.ink}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.on-dark}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 26px"
    height: "56px"
  input-text:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "13px 14px"
    height: "52px"
  chip:
    backgroundColor: "{colors.field}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "0 18px"
    height: "48px"
  chip-selected:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.card}"
  form-card:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.card}"
    padding: "clamp(20px, 5vw, 32px)"
  photo-card:
    backgroundColor: "{colors.field}"
    textColor: "{colors.card}"
    rounded: "{rounded.card}"
  step-number:
    backgroundColor: "{colors.brass}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    size: "48px"
  float-message:
    backgroundColor: "{colors.brass}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    size: "60px"
---

# Design System: Scott J. D'Antonio Inc.

## Overview

**Creative North Star: "The Freshly Finished Room"**

The site is a house after Scott has been through it: clean off-white walls, painted navy trim, and one run of warm brass hardware that catches the eye. Order is how it earns trust. Full-bleed bands alternate light and dark so each new part of the page is obvious on a phone, the shapes are soft and borderless, and nothing competes with the one brass accent. It's a single-page persuade surface for a local trade, built phone-first for Facebook's in-app browser, and it follows Ellie's house calm band style.

Density is low and the pace is even: one idea per band, generous band padding, short headings set in a single display face. Motion is limited to three things: the hero headline bouncing in letter by letter, one 12px fade-up for content below the first screen, and the floating message circle sliding in. Every one of them is skipped under reduced motion and without JS, and nothing is ever left hidden at rest.

Photography is currently AI-generated example imagery (gpt-image-1, 2026-10-21) under navy overlays and gradients. It shows the kind of work, never Scott's own jobs, and it should be swapped for real job photos when they exist, using the same overlay treatments.

The small eyebrow pills above the hero headline and the quote heading come from Ellie's house calm band style as her own exception. They're governed by that house file, not by this system, so they aren't specified here as a component.

**Key Characteristics:**
- Paper, two navies, one brass accent; the ground is never black.
- Full-bleed bands in a paper / navy / deep / paper / navy rhythm, with the deep bands carrying a faint diagonal line texture.
- One display webfont (Cal Sans, weight 400) for headings, labels and buttons; the system stack for running text at 16/1.7.
- Soft, borderless forms: 24px cards, full pills, 10px tinted fields.
- Hover only where there's a real pointer; on photo and Facebook rows, only the arrow circle changes.

## Colors

A cool slate-navy system on off-white paper, with a single warm brass accent used as a fill.

### Primary
- **Hardware Brass** (brass): the only accent. Primary button fills, the floating message circle, step numbers, the Facebook row, claim icons on navy, the accent phrase in dark-band headings, and the selection highlight. Text on it is always Ink.
- **Polished Brass** (brass-2): the hover state of brass fills only.
- **Brass Ink** (brass-ink): brass when it has to be text or an icon on a light ground (the header Messenger icon and its hover). It's about 5.8:1 on paper; raw brass on light fails contrast.

### Neutral
- **Slate Navy** (navy): the mid-dark band ground (trust band, closing band). Also serves as the textarea caret.
- **Deep Navy** (deep): the darkest band ground (how it works, footer) and the base of the hero and photo overlays. It carries the diagonal line texture.
- **Ink** (ink): headings on light, text on brass, the selected chip fill. Same value as Deep Navy, used in a text role.
- **Body Slate** (body): running text on light grounds.
- **Soft Slate** (soft): ledes, helper text, the wordmark subline, "(optional)" hints.
- **Wall Paper** (paper): the page ground, header and light bands; also the inset ground of the post-submit panel.
- **Card White** (card): the form card. White also carries the hero H1, photo card titles and selected chip text.
- **Field Tint** (field): fills for inputs and chips on the white form card, and the placeholder ground of photo cards.
- **On-Dark** (on-dark) and **On-Dark Soft** (on-dark-soft): headings and running text on navy and deep bands.
- **Focus Navy** (focus): hover and focus outlines on light grounds. It has the same value as Slate Navy but is a separate token so focus can never be confused with the brass fill.
- **Error Red** (error): invalid field borders and the plain-sentence error message.

### Named Rules
**The Brass Is Hardware Rule.** Brass is a fill, never text on a light ground. Text on brass is Ink; brass as text on light is Brass Ink. If brass is the only thing marking an element, check it against the ground before shipping.

**The Accent Phrase Rule.** On dark grounds (hero, navy, deep), a heading may end with its last phrase in brass ("refreshed.", "like mine.", "works."). Headings on paper stay all Ink.

**The Faint Lines Rule.** The deep-band texture is `repeating-linear-gradient(135deg, transparent 0 22px, rgba(255,255,255,.035) 22px 23px)` and appears only on Deep Navy grounds. Keep it at about 4% white or fainter so it never reads as lines through text.

## Typography

**Display Font:** Cal Sans (with Avenir Next, Segoe UI, system-ui)
**Body Font:** System stack (-apple-system, BlinkMacSystemFont, Segoe UI, Helvetica Neue, Arial)

**Character:** A rounded, friendly geometric display face at one weight carries every heading, button, field label and link phrase, so the voice stays consistent and approachable. The native system face does the reading underneath, quiet and fast on the phone.

### Hierarchy
- **Display** (400, clamp 42–80px, 1.02): the hero H1 only, white, capped at 11ch so the place name lands on its own line.
- **Headline** (400, clamp 30–48px, 1.08): one per band, balanced wrapping.
- **Title** (400, about 20–28px, 1.1–1.2): photo card titles, trust claims, step titles (21px, 22px from 1024px), the Facebook row. The closing "Message me" link is an oversized title (clamp 28–44px).
- **Lede** (400, clamp 17–19px, 1.7): one sentence under a headline, Soft Slate on light, max 40ch. The hero promise is the same role at clamp 17–20px, 1.5, max 30ch (40ch on desktop).
- **Body** (400, 16px, 1.7): all running text and inputs. Inputs never go below 16px so iOS doesn't zoom.
- **Label** (400 Cal Sans, 17px, 1.2): form labels and legends. Buttons use Cal Sans at 18px / 1.

### Named Rules
**The One Weight Rule.** Cal Sans is only ever set at 400. Emphasis comes from size and the brass accent phrase, not weight. Inside body text, `<b>` is the system face at 600.

**The Two Faces Rule.** One display webfont, one system body stack. Never add a second body or display family.

## Layout

A single centered column, max 1160px, with a 20px gutter on phones and 40px from 760px. Bands are full-bleed with 64px vertical padding on phones and 96px from 760px. A band's heading block (headline plus lede, 16px gap) is capped at 640px.

Breakpoints: 760px (desktop layout, larger header, buttons side by side at min 240px, two photo cards in a row up to 880px) and 1024px (two-column splits: the trust band puts its claims in the right column; the quote band pins its heading block as a sticky left column at 1fr / 1.2fr with a 64px gap; the closing band puts the big Messenger link at the bottom right; the three steps go into a row with 40px gaps). Below 380px, chips get tighter padding.

Rhythm inside bands: 16px between cards and stacked items, 20px between form fields and hero items, 28–36px between a heading block and the content under it. Tap targets are 44px or larger everywhere, including footer links and the wordmark.

## Elevation & Depth

The system is flat. Depth comes from the alternating light and dark bands, the white form card sitting on paper, and navy gradients over photographs. The only shadow is on the floating message circle, because it's the only thing that floats over the content.

### Shadow Vocabulary
- **Float** (`box-shadow: 0 10px 28px rgba(8,24,46,.3)`): the floating message circle only.

### Named Rules
**The Flat Bands Rule.** Cards, buttons and fields have no shadow at rest or on hover. Separation comes from colour, band changes and tinted fills. Hard offset shadows don't belong here.

**The Navy Veil Rule.** Photos sit under Deep Navy. The hero gets a top-to-bottom gradient on phones (about .90 to .74) and a left-to-right one on desktop (about .92 to .50), so white text always sits on the dark side. Photo cards get a bottom gradient from transparent at 45% to about .86. Check that white text is 4.5:1 or better on the actual pixels.

## Shapes

Soft and borderless. Containers use the 24px card radius, every button and chip is a full pill, inputs use a 10px radius on a tinted fill with a transparent 2px border that only shows on hover, focus or error. Circles are used for the arrow buttons (44px), step numbers (48px) and the floating message button (60px). Dividers appear in exactly one place: hairlines between trust claims on navy (1px, 14% white). Icons are inline SVG line drawings, about 2.1–2.6 stroke with round caps, sized 18–28px in controls and 40px for the trust claims.

## Components

### Buttons
Confident, round and tactile; there are never more than two side by side.
- **Shape:** full pill (999px), 56px tall, 26px side padding, Cal Sans 18px, an optional 20px leading icon.
- **Primary:** Hardware Brass fill, Ink text. Hover goes to Polished Brass. Used for "Get a quote", the form submit and "Open Messenger". Inside the form it's full width.
- **Ghost:** transparent with a 2px 70% white border and On-Dark text, used on the hero only. Hover turns the border solid white with a 10% white wash.
- **Line:** transparent with a 2px Ink border on light grounds ("Copy again"). Hover adds a 6% Ink wash.
- **Press / Focus:** scales to .98 on press. Focus is a 3px outline 3px out, Focus Navy on light and brass on dark. Inside the form, hover also adds a 2px Focus Navy outline.

### Chips
- **Style:** Field Tint pill, 48px tall, 2px transparent border, system 16px Ink text. These are radio buttons styled as pills.
- **State:** selected chips are filled Ink with white text. Hover shows a Focus Navy border; a selected chip shows a 2px outline 2px out, because a navy border on the Ink fill would be invisible. Tapping a photo card picks the matching chip.

### Cards / Containers
- **Form card:** Card White, 24px radius, clamp 20–32px padding, 20px gap between fields, max 600px.
- **Post-submit panel:** a paper inset inside the form that holds the composed message in a read-only white textarea, with Primary and Line buttons.
- **Shadow Strategy:** none (see Elevation & Depth).

### Inputs / Fields
- **Style:** Field Tint fill, 10px radius, 2px transparent border, 52px minimum height (textarea 120px), system 16px Ink text. Each one has a `for`-linked Cal Sans label above it.
- **Focus / Hover:** the border becomes Focus Navy. No glow.
- **Error:** an Error Red border that still wins while the field is focused, plus a plain-sentence message in Error Red at 16px under the field. The error clears as soon as the visitor types.

### Navigation
- **Header:** a paper strip, 64px tall (76px from 760px). The wordmark sits on the left: the name in Cal Sans 20/24px over a 12px 600 uppercase Soft Slate subline at .08em ("Inc. · Marlton, NJ"). "Message me" sits on the right in Cal Sans 17/20px with a Brass Ink icon and turns Brass Ink on hover. There's no menu.
- **Footer:** Deep Navy with the line texture. Underlined On-Dark links with a 4px offset and a 40% underline, turning brass on hover.

### Photo Card (signature)
A 4:5 photo link with a 24px radius and a bottom Deep Navy gradient. The white Cal Sans title sits at the bottom left and a 44px arrow circle (18% white) at the bottom right. On hover or focus only the arrow changes: it fills with brass and its arrow turns Ink. Focus also adds a brass ring around the arrow. Two of them sit side by side from 760px.

### Facebook Row (signature)
A brass panel up to 460px wide, at least 76px tall, with a 20px radius. It holds the Facebook glyph, a Cal Sans 19–22px line and an arrow circle at 12% Ink. On hover the arrow circle turns Ink with a brass arrow.

### Numbered Steps (signature)
A CSS-counter list. Each step has a 48px brass circle with a Cal Sans Ink numeral, a Cal Sans title in On-Dark and one line of soft text. They stack on phones and sit in three columns from 1024px.

### Floating Message Circle (signature)
A 60px brass circle with an Ink Messenger icon, fixed 16px from the bottom right inside the safe area, with the Float shadow. It slides up (.35s, cubic-bezier(.2,.8,.2,1)) once the hero has scrolled away, and hides again while the quote form or the closing band is on screen. While hidden it's taken out of the tab order and aria-hidden. There's only ever one circle, never a bottom bar.

### Hero Headline Bounce-In (signature motion)
On the hero H1 only, each letter slides in from 50px to the right over 1s with cubic-bezier(.34,1.56,.64,1), 20ms apart, wrapped by word so words never break. When the last letter lands, the plain heading is restored. The split is skipped without JS and under reduced motion.

## Do's and Don'ts

### Do:
- **Do** use brass only as a fill, with Ink text on it; use Brass Ink when brass has to be text on light.
- **Do** alternate full-bleed light and dark bands, and only put the diagonal texture on Deep Navy.
- **Do** keep every interactive target 44px or larger and every input at 16px or larger.
- **Do** put hover styles inside `@media (hover:hover)` so taps don't leave them stuck on.
- **Do** outline form controls on hover and focus with Focus Navy on light grounds and brass on dark grounds.
- **Do** keep the fade-up at 12px over 400ms, and only on elements that start below the first screen; everything stays visible at rest, without JS and under reduced motion.
- **Do** put every photo under a Deep Navy overlay or gradient and check white text at 4.5:1 or better.

### Don't:
- **Don't** set brass text, or white text, on light grounds, or white text on brass.
- **Don't** add shadows to cards, buttons or fields; the Float shadow belongs to the floating circle only.
- **Don't** set Cal Sans in any weight but 400, or add a second display or body family.
- **Don't** give the letter bounce-in to any heading other than the hero H1.
- **Don't** let more than two buttons share a row, or add a second floating control or a bottom bar.
- **Don't** present the example images as Scott's own jobs.
