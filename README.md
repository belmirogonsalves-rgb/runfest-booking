# RunFest Norway — Booking Flow Prototype

A redesigned race **registration / booking flow** for **RunFest Norway** (2–3 October, Oslo).
The live event registration currently runs on the third‑party **EQ Timing** platform — its timing
backend (hardware, runner badges/trackers) is kept; only the **front end of the booking process**
is reimagined here.

This is a clickable, self‑contained **HTML + Tailwind** prototype.

## Goals of the redesign

- **Selection-based, not cart-based** — tap races to add/remove, no confusing basket.
- **Pricing upfront** — every race shows its price, auto‑resolved to each runner's age bracket
  (no more cross-referencing a separate "Information" tab).
- **Fewer steps** — `Select → Pay → Done` instead of a 4+ click cart maze.
- **Guest-first checkout** — pay as a guest with **Vipps** (1‑tap, the express path in Norway) or
  card; account creation offered *after* payment.
- **Mobile-first** — sticky bottom bar + bottom-sheet summary.
- Nothing removed from the original flow — only improved.

## Run it

It's a single static file. Either open `index.html` directly in a browser, or serve it:

```bash
python -m http.server 4599
# then open http://localhost:4599
```

## Flow

1. **Choose your races** — filter by day / distance / timed vs untimed, add multiple runners
   (each priced by age), single races + money-saving bundles.
2. **Pay** — guest contact details, Vipps or card, live order summary.
3. **Confirmation** — optional account creation.

## Tech

- HTML5, Tailwind CSS (Play CDN), vanilla JS — no build step.
- Fonts: Barlow Condensed (display) + Barlow (body).

## Status

Prototype for stakeholder/EQ Timing review. The production target is to run this front end on top
of EQ Timing's registration **API**.
