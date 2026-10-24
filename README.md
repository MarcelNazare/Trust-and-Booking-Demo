# Lusaka Shine Pros — Trust & Booking Demo

> **Concept demo — not a client project.** This site was built to show a
> cleaning or professional services business what a conversion-focused
> website looks like when it's done properly. It is not a live business.
> Every testimonial, rating, and price on the page is fictional.

---

## What this is

A multi-page, mobile-first demo website for a fictional cleaning company
in Lusaka. Its job is to demonstrate one thing: **how a service business
turns a curious visitor into a booked job or a WhatsApp enquiry.**

It is the first of three demos in the portfolio, and the strongest
all-rounder. Cleaning, professional services, home services, salons —
any business where the customer is inviting a stranger into their home,
office, or body needs to solve the same problem: **trust before
transaction.** This demo is built around that problem.

| | |
|---|---|
| **Fictional client** | Lusaka Shine Pros |
| **Niche** | Cleaning & professional services |
| **Primary outcome sold** | Booked jobs and WhatsApp enquiries |
| **Design system** | Claude DESIGN.md (from `VoltAgent/awesome-design-md`) |
| **Stack** | Multi-page HTML, embedded CSS, Inter/StyreneB fallback, no build step |
| **Hosting** | Free tier (Vercel / Netlify) |
| **Status** | Concept demo — placeholder content throughout |

---

## Why this demo exists

A cleaning customer has three questions before they pick up the phone:

1. **Can I trust these people in my home or office?**
2. **What does it cost, roughly, before I call?**
3. **How do I actually book?**

Most cleaning business websites in Lusaka fail at all three. There are
no prices, no real testimonials, and the only way to book is to find a
phone number. The demo answers all three on the page, then hands the
visitor a WhatsApp button.

The sales line for this demo is:

> *"I built a concept for a cleaning business. There are real prices on
> the page, testimonials from actual neighbourhoods, and a WhatsApp
> button that works. Want me to build the real one with your services
> and your prices?"*

It replaces "do you have a portfolio?" with a live, clickable answer to
the only question a cleaning business owner will have: *"will this
actually get me bookings?"*

---

## Key features

### 1. Conversion-focused layout
- **"Get a Quote" and "Book Now"** buttons appear above the fold, after
  each service section, and in a **sticky bottom bar on mobile** —
  thumb-reachable, always visible.
- The primary CTA is consistent across every page: **"Get a free quote
  on WhatsApp."** One action, repeated. No "Contact Us" page, no
  generic form that goes nowhere.
- Every service card has its own CTA, so a visitor reading about
  "Deep Cleaning" can book without scrolling back up.

### 2. Trust-building elements
- **A dedicated testimonials section** with client names and
  neighbourhoods (e.g., "Chilenje," "Kabulonga," "Woodlands") — specific
  locations build more trust than "Happy Customer, Lusaka."
- **Client ratings** shown as a simple aggregate line near the hero
  ("Trusted by 200+ Lusaka homes and offices"), not as fake 5-star
  badges on every card.
- **Trust badges**: a real business registration line in the footer
  ("Registered with PACRA"), a simple "Police-cleared staff" line near
  the booking CTA. No logo walls, no fake accreditations.
- **Before/after gallery**: a small grid of cleaning photos (placeholder
  images in the demo) that shows the work, not stock photos of smiling
  people in aprons.

### 3. Clear service & pricing guidance
- **Distinct sections** for Residential Cleaning, Office Cleaning, and
  Deep Cleaning.
- Each section shows a **starting price** ("From K350") and a short
  bullet list of what's included. No hidden prices, no "call for
  quote."
- Transparent pricing **pre-qualifies leads** — the visitor who can't
  afford K350 self-selects out, and the one who can arrives already
  warm.

### 4. Mobile-first & WhatsApp integration
- The page is **built for a phone first**. The demo loads in under two
  seconds on a 3G connection (no heavy images, no external scripts
  beyond fonts).
- A **click-to-chat WhatsApp button** appears in the header and as a
  sticky bottom bar on mobile. It opens WhatsApp with a pre-filled
  message: *"Hi Lusaka Shine Pros, I'd like a quote for [service]."*
- This is the baseline expectation in the Zambian market. A cleaning
  business without WhatsApp click-to-chat is leaving bookings on the
  table every day.

---

## Design decisions

The page is built on the **Claude DESIGN.md** system. Why Claude and
not Stripe (used for the consultancy demo) or Vercel (used for the car
hire demo):

| Requirement | Why Claude fits |
|---|---|
| Trust must be felt, not claimed | Claude's warm cream canvas and coral accent feel human, not corporate |
| The page must welcome, not intimidate | Claude's editorial layout is approachable, not stark |
| The customer is inviting a stranger in | Warmth in the palette and typography counteracts the natural anxiety |
| Mobile reading must be comfortable | Claude's typography is tuned for long-form reading on small screens |

**Constraints carried over from the design system:**

- **Canvas**: cream (`#faf9f5`), not pure white. This is the single
  biggest trust signal on the page — it reads as a small business,
  not a fintech startup.
- **Accent**: coral (`#cc785c`), used only for the primary CTA, the
  starting prices, and the sticky WhatsApp bar. No other color appears
  on the page except text and borders.
- **Typography**: StyreneB (Inter fallback). Body at 16px, weight 400.
  Headings at weight 500 — not bold. Bold reads as aggressive;
  weight 500 reads as confident.
- **Rounded corners**: 8px on buttons, 12px on cards. Soft enough to
  feel approachable, not so soft it looks like a toy.
- **No shadows** on cards. Depth comes from the cream-vs-white surface
  contrast and a hairline border.

**What was deliberately avoided:**

- Stock photos of smiling cleaners in aprons (the single biggest
  "AI-generated local business site" tell)
- Star ratings on every testimonial (one aggregate line is enough)
- A logo wall of "trusted by" brands (cleaning businesses don't have
  logo walls; they have neighbourhood names)
- A contact form that goes to an email nobody checks
- Hidden prices and "call for a quote" copy
- Decorative icons on every service card

---

## File structure

```
/
├── index.html          # Home — hero, trust strip, services, testimonials, CTA
├── residential.html    # Residential cleaning — pricing, what's included, CTA
├── office.html         # Office cleaning — pricing, what's included, CTA
├── deep-clean.html     # Deep cleaning — pricing, what's included, CTA
├── contact.html        # Booking / quote page — WhatsApp + short form
├── styles.css          # Shared styles (or embedded per-page if single-file)
└── README.md           # This file
```

No build step. No dependencies beyond the StyreneB or Inter font. Open
`index.html` in a browser, or deploy the folder to any static host.

The WhatsApp click-to-chat link is generated with the standard
`https://wa.me/<number>?text=<url-encoded-message>` pattern. Replace the
placeholder number in `index.html` and `contact.html` with the real one
when you hand the demo over.

---

## How to use this demo in a sales conversation

1. **Identify a cleaning or professional services prospect** with a
   weak site — no prices, no WhatsApp, no testimonials.
2. **Send the link** with a one-liner referencing something specific:
   *"I noticed your prices aren't on your site — here's a concept that
   puts them front and centre."*
3. **Say the line:** *"Real prices, real testimonials, and a WhatsApp
   button that works. Want me to build this with your services?"*
4. **If they reply,** book a call and use the demo as the visual brief.

The demo is **not** sent cold to every business. It is sent to cleaning
and service businesses, and only after you've looked at their current
site and found a specific gap the demo closes.

---

## Roadmap (next build steps)

- [ ] **Wire the WhatsApp link** to a real number and pre-filled message
  for each service. Test on iOS and Android.
- [ ] **Wire the quote form** on `contact.html` to a real endpoint
  (Formspree, Google Sheets via Apps Script, or a simple serverless
  function) with an auto-reply email.
- [ ] **Add a before/after gallery** with real (or licensed) photos of
  cleaning work. This is the single most trust-building element on the
  page and it is currently a placeholder.
- [ ] **Add a simple booking calendar** on the contact page — even a
  Calendly embed is enough to remove one more step from the visitor's
  path.
- [ ] **Build a Google Business Profile** for the fictional business as
  a proof-of-concept, so the demo can also show how the site and the
  profile work together in local search.
- [ ] **Build a second variant** for a different service niche
  (e.g., pest control, landscaping) to A/B the pitch.

---

## Reusing this demo for other service niches

The structure is deliberately generic enough to retarget:

| Element | Change for a new niche |
|---|---|
| Brand name | Swap `Lusaka Shine Pros` |
| Hero H1 | Rewrite around that niche's trust problem |
| Services | Replace cleaning tiers with the new niche's services |
| Starting prices | Change to the new niche's pricing unit |
| Testimonials | Rewrite with neighbourhoods and service-specific detail |
| Before/after gallery | Replace with photos of that niche's work |
| WhatsApp message | Change the pre-filled text to match the new service |

Keep the design system. Change the content. The demo is the **shell**;
the niche is the **fill**.

---

## Honesty note

This is a **concept demo**, not a real business. Every testimonial,
rating, price, neighbourhood, and phone number on the page is
fictional. The WhatsApp button in the demo opens a placeholder chat.

The footer carries the line *"Concept demo — not a client project"* so
that anyone landing on it understands what they're looking at.

If you reuse this demo for a real client, remove that line, replace
every placeholder, wire the WhatsApp link and the quote form to real
destinations, and test the whole booking flow on a phone before
publishing.
