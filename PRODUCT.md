# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Dragon boat paddlers doing year-round gym training, on their phones, usually in the gym between sets.

- **All athletes (the app):** team athletes and individual members use the same app. Every app screen is designed for both equally. Team athletes see their team logo; members see the DB Speed seal.
- **Paying individuals (the join page):** the join page is for individuals deciding to pay. This is the growth focus.

## Product Purpose

DB Speed gives dragon boat paddlers a year-round gym program in a phone app, plus a Skool community. Athletes open today's session, log their sets, and follow their progress through the season. A new week arrives every Monday.

## Positioning

Built and coached by Martin Shih: Team Canada Premier world champion and kinesiologist (McGill), who has coached athletes to the World Championships and coached 22 Dragons to CCWC gold. Bilingual, English and French.

- Dragon boat specific: programming built for paddlers and their season.
- A real coach behind it: Martin writes the programs and answers directly.
- A year-round season plan, with a new week every Monday.
- A community of paddlers on Skool.

## Operating Context

- The app opens from a private link per athlete, added to the phone's home screen.
- Joining: Stripe checkout, a 1-minute form with the same email, the app link by email, then Skool with 3 join questions using the same email.
- Programs and logged results sync with a Google Sheet through a Google Apps Script API.
- Weekly use: Today, Program, Progress, Guide and Season tabs, a rest timer, a workout timer, and team circuits run from a shared timer.
- Form Check Friday gives video feedback on lifts.
- Members whose payment stops see a paused-membership screen with a restart button.

## Capabilities and Constraints

- Static site on GitHub Pages at app.dbspeed.app, with no build step: `index.html` (app), `join/`, `join/fr/`, `privacy/`.
- Plans in CAD: Weekly $35, Monthly $140, Yearly $1,390. Outside Canada, checkout shows US dollars.
- PERG, OC and mobility are coming soon and not included yet. Do not present them as available.
- Terms: "DB Speed", "Form Check Friday", "Team circuit".

**Rules for design work:**

- Change styles and layout only. Never change JavaScript logic, saving, API or device code.
- Work on a separate git branch with a preview. Never commit to main.
- Never put athlete data or app codes in the repo.

## Brand Commitments

- Keep the current look: dark scoreboard theme, Barlow fonts, one red accent.
- Logo: the DB Speed lane seal.
- French uses vous on public pages and tu in personal messages.
- Martin writes in the first person on the privacy page.

## Evidence on Hand

Usable publicly:

- Martin Shih's credentials and coaching results, as stated in Positioning.
- Team results for Immortals and 22 Dragons. Name only these two teams publicly until other teams agree.
- The strength standards (Entry to NT Strong).
- Athlete testimonials, which Martin can supply, collected with written permission. Use only real quotes supplied by Martin. Until then, leave them out.

Never invent or imply:

- Never invent a testimonial or quote.
- Never show real athlete names, numbers or results without their permission.

## Product Principles

- One app for every athlete: no screen favours team athletes or individual members.
- The join page sells to individuals, on real credentials and results only.
- Readability in the gym comes before expression.
- Public claims are only what can be proved and what teams and athletes have agreed to.
- English and French are equal: no athlete-facing surface ships in one language only.

## Accessibility & Inclusion

- Every athlete-facing surface is phone-first and ships in English and French.
- Text contrast of at least 4.5:1.
- Tap targets of at least 44px.
