# Scott J. D'Antonio Inc. — handoff at ~60%

**Live:** https://10elizabethbell.github.io/dantonioRemodeling/ · **Repo:** https://github.com/10elizabethbell/dantonioRemodeling · **Built:** 2026-10-21 from Muse brief of 2026-10-21 (thin brief) · **Call Sheet:** site set (entry added; Muse hadn't created one)

## What's built
- One page in the calm band style, with bands in this order: paper header, photo hero, paper "Inside and out." (two 4:5 photo cards), navy "I treat your home like mine." (three claims plus a big brass "See my work on Facebook." row), deep-navy "How it works." (3 steps), paper quote form, navy close, deep-navy footer.
- Palette (no logo exists, so this is my choice): paper #f4f6fb, slate navy #23415f, deep navy #142a42, warm brass #e3a83b as the fill accent, and #835700 for brass text on light. Headings are Cal Sans.
- Hero: a generated example kitchen under a deep-navy overlay. On phones it's a portrait crop and the overlay is darker; on desktop the overlay fades lighter to the right. The H1 "Your South Jersey home, refreshed." bounces in letter by letter.
- **Contact is Facebook Messenger only** (`https://m.me/100095065165107`; I checked that it resolves to the page's message thread). It shows up as:
  - "Message me" in the header's top-right corner, where the phone number would normally go
  - the floating circle, which opens Messenger
  - the closing band's big "Message me"
  - the quote form, which writes out the message, copies it, shows it in a read-only box, and offers "Open Messenger" plus "Copy again"
- Every Messenger link also passes `?text=` with the message, in case Messenger pre-fills it (not guaranteed). Without JS the form is replaced by a plain Messenger button.
- Fade-up on sections below the first screen. Under reduced motion and with JS off, everything shows at once (checked in Chromium and WebKit).

## Assumptions I made
- **Owner's first name "Scott"**: inferred from the company name. The page speaks as "I'm Scott".
- **New facts not in the brief**, from the Facebook page's meta tags read 2026-10-21: based in **Marlton, NJ**, **"Established in 1997"**, and **"Interior/exterior home improvements"**. Muse didn't have these.
- **Services**: kept to what's published ("Light & cosmetic remodeling", interior and exterior). I didn't invent an itemised list.
- **Towns**: Cherry Hill, Moorestown, Mt. Laurel and Voorhees come from Muse's garbled OCR of the promo image and haven't been checked. Only Marlton is confirmed.
- **Care copy**, written in his voice, not his words:
  - "I treat your house the way I'd want someone to treat mine."
  - the three steps, including "I come and see it", which assumes he visits before quoting
  - "Small jobs welcome" (form eyebrow)
  - "Not sure it's something I do? Ask anyway."
- **"Get a quote", not "free quote"**: nothing says his quotes are free.
- **Colours**: none published. Brass on navy suits trim and hardware, and it's easy to swap in the `:root` tokens.

## Placeholders and gaps
- **No phone and no email**: nothing is published (Muse searched, and so did I via Facebook meta). The header uses "Message me" instead of a number, and the footer has no email. If Scott gives a number, the header should show it as a tap-to-call link, the floating circle and the form should switch to `sms:`, and Messenger can stay in the footer.
- **No client photos.** All three photos are generated (table below) and presented only as examples: the hero has empty alt text, and the card alts say "An example of…". They should be swapped for his real jobs as soon as possible, because the cards sit right before "See my work on Facebook." and could still read as his work.
- **Promo image not fetched**: the group post needs a Facebook login (the crawler only returns the group's cover). Someone logged in should check the towns and any service list on it.
- **No logo.** The favicon and home-screen icon are a brass "SD" on deep navy, set in my own lettering.
- **Facebook timeline not seen.** "See my work on Facebook." assumes his page has job photos. If it doesn't, change the row to "Find me on Facebook."
- Hours, reviews, prices and licence number are unknown, so none of them appear on the page.

### Images
| File | Shows | Source | Prompt (short) | Licence |
|---|---|---|---|---|
| img/hero-wide.webp, img/hero-tall.webp | Refreshed white shaker kitchen, oak floor | generated with gpt-image-1, 2026-10-21 | real-estate photo, refreshed kitchen in an older NJ colonial, subway tile, crown molding, daylight | generated; OpenAI terms assign output to the user |
| img/bath.webp, img/bath-900.webp | Updated hall bathroom, white vanity, grey walls | generated with gpt-image-1, 2026-10-21 | real-estate photo, updated 1970s split-level bathroom, overcast window light | same |
| img/porch.webp, img/porch-900.webp | Refreshed colonial front porch, navy door | generated with gpt-image-1, 2026-10-21 (garbled caption strip cropped off) | real-estate photo, refreshed porch, white columns, grey boards, no house number | same |
| og.jpg | Link preview: hero kitchen plus headline | rendered from the hero | — | same |

His Facebook profile photo (a smiling man in front of a stone wall, presumably Scott) is in `src-assets/logo-og.jpg`. I didn't use it, because I can't confirm it's him. A small round portrait beside "I treat your home like mine." would add a lot of trust once he says yes.

## Questions for the owner
1. Is there a phone number you'd like customers to call or text?
2. Which jobs do you do most, and which do you want more of? (kitchens, baths, trim, paint, flooring, decks, siding…)
3. Can we use photos of your jobs from Facebook, and your profile photo?
4. Which towns do you cover? Is the list on your promo image right?
5. Do you give free estimates? Are you licensed and insured? (NJ HIC number?)
6. Is it just you, or do you have a crew? That decides whether the page says "I" or "we".
7. An email for the footer?

## Ideas not built (yours to pick)
- **Runner-up signature motion (opt-in):** "fresh paint". A slow brass roller stroke wipes across the hero's bottom edge and leaves a crisp new-paint line, and a finger or mouse can roll more paint across a dull wall. Other worlds I considered: wiping old wallpaper away, a sanded-wood grain revealing, sharp caulk lines, a tape line peeling off to show a clean edge.
- Before/after sliders as soon as he has paired photos.
- A portrait and his first-person story ("Since 1997…") in the trust band.
- Flagged by Impeccable but kept by house rule:
  - eyebrow pills (craft-floor ban)
  - the H1 bounce easing (animate and quieter modes)
  - the diagonal band texture (detector "repeating-stripes-gradient"; ignored for this file in `.impeccable/config.json`)
  - Cal Sans
  - the floating circle
- Detector "flat type hierarchy": ignored for this file. It only counts the fixed 12–20px UI sizes, and the headings are fluid (`clamp`) at 30–80px.
- Sweep suggestion not taken: restyle the submit button as "Update message" after sending. I hide it instead and bring it back when the visitor edits the form.

## Not verified
- Messenger handoff on real phones: whether `m.me` opens the Messenger app or the in-browser chat from inside Facebook's in-app browser, and whether `?text=` pre-fills it. The copy-and-paste path is the fallback, and I only tested it headlessly. The clipboard may be blocked in the Facebook in-app browser, but the message stays on screen to copy by hand.
- Real-device touch, and frame rate on old phones (motion is limited to the H1 and the fade-up).
- How the link preview looks when the URL is posted on Facebook.
