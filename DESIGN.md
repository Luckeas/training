---
name: DB Speed
description: Year-round gym training for dragon boat paddlers, read like a race scoreboard.
colors:
  accent: "#d64124"
  accent-ink: "#ffffff"
  accent-text: "#ee6146"
  blue: "#5089e2"
  rest: "#376fcb"
  rest-ink: "#ffffff"
  amber: "#f2b233"
  good: "#43c08a"
  good-ink: "#06150e"
  bg: "#121315"
  surface: "#1b1d20"
  raised: "#24272b"
  line: "#30343a"
  fg: "#f3efe6"
  muted: "#9b9a93"
  faint: "#8e8f92"
typography:
  display:
    fontFamily: "Barlow Condensed, Arial Narrow, Helvetica Neue, Arial, sans-serif"
    fontSize: "92px"
    fontWeight: 800
    lineHeight: 0.82
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "Barlow Condensed, Arial Narrow, Helvetica Neue, Arial, sans-serif"
    fontSize: "44px"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "0.01em"
  title:
    fontFamily: "Barlow Condensed, Arial Narrow, Helvetica Neue, Arial, sans-serif"
    fontSize: "24px"
    fontWeight: 700
    lineHeight: 1.02
    letterSpacing: "0.03em"
  body:
    fontFamily: "Barlow, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "Barlow Condensed, Arial Narrow, Helvetica Neue, Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 700
    letterSpacing: "0.12em"
rounded:
  xs: "6px"
  sm: "10px"
  md: "12px"
  lg: "14px"
  xl: "20px"
  pill: "999px"
spacing:
  xs: "6px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "18px"
  2xl: "22px"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.accent-ink}"
    rounded: "{rounded.md}"
    padding: "14px 18px"
  button-ghost:
    backgroundColor: "{colors.raised}"
    textColor: "{colors.fg}"
    rounded: "{rounded.md}"
    padding: "14px 18px"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.fg}"
    rounded: "{rounded.lg}"
  input:
    backgroundColor: "{colors.raised}"
    textColor: "{colors.fg}"
    rounded: "{rounded.sm}"
    height: "44px"
  chip:
    backgroundColor: "{colors.raised}"
    textColor: "{colors.muted}"
    rounded: "{rounded.xs}"
    padding: "3px 8px"
  phase-pill:
    backgroundColor: "{colors.raised}"
    textColor: "{colors.fg}"
    rounded: "{rounded.pill}"
    padding: "5px 10px"
  state-done:
    backgroundColor: "{colors.good}"
    textColor: "{colors.good-ink}"
    rounded: "{rounded.xs}"
    padding: "4px 8px"
  tab:
    textColor: "{colors.faint}"
    padding: "10px 4px 12px"
  tab-active:
    textColor: "{colors.fg}"
---

# Design System: DB Speed

## Overview

**Creative North Star: "The Race Scoreboard"**

DB Speed reads like the board at a regatta finish: dark, loud where it counts, and legible from a distance. The week number is the biggest thing on the Today screen, the season is a bar of 32 lit cells, and a logged set turns green like a result going up. An athlete between sets should get what they need in one glance, with a sweaty thumb, without reading a sentence.

The system is dense but calm. Condensed uppercase type carries the numbers and labels, a plain humanist body carries the sentences, and everything sits in one phone-width column. Colour is rationed and means something: red says what is current or what to press, green says done, amber says caution or target, blue says rest and focus.

Depth is flat and firm. Surfaces separate by tone and a thin border, and controls feel solid rather than floating. The join and privacy pages share the same fonts, palette and card language, so the public pages and the app read as one product.

**Key Characteristics:**
- Numbers are the heroes: condensed, heavy, tabular.
- One phone-width column with a sticky top bar and fixed bottom tabs.
- Flat tonal layers with hairline borders.
- One accent per screen, with colour used for status rather than decoration.
- Uppercase condensed labels for structure, sentence-case Barlow for reading.

## Colors

A warm near-black scoreboard with cream text, one hot red accent, and three status colours.

### Primary
- **Finish-Line Red** (accent): The one accent, as a fill or line. Primary buttons, the current week and featured-day border, the active tab icon, and the phase dot.
- **Button White** (accent-ink): Text on Finish-Line Red.
- **Red Text** (accent-text): The same hue lifted for reading, used whenever the accent is text. In the app it is derived from the accent, so team colours stay readable.

### Secondary
- **Rest Blue** (rest): The rest timer fill, with its own ink (rest-ink).
- **Signal Blue** (blue): Focus outlines and coach notes inside a set target.

### Tertiary
- **Target Amber** (amber): Superset flags, partly finished days, the next benchmark target, warnings, and the add-to-home-screen banner.
- **Result Green** (good): Done sets, finished days, sync status, hit benchmarks, and the workout progress bar.
- **Green Ink** (good-ink): Text on Result Green.

### Neutral
- **Scoreboard Black** (bg): The page behind everything.
- **Panel Charcoal** (surface): Cards, the tab bar, and sheets.
- **Raised Graphite** (raised): Inputs, ghost buttons, chips and pills, one step up from a card.
- **Hairline** (line): Borders, dividers, and unlit week cells.
- **Cream** (fg): Primary text.
- **Weathered Grey** (muted): Secondary text and labels.
- **Dim Grey** (faint): Placeholders, set numbers, and inactive tabs.

### Skins and team colour

Scoreboard is the system, and everything above describes it. Daylight (light, red) and Lake (dark teal, amber accent) remain optional looks in settings, with complete palettes in the app stylesheet. Design new work for Scoreboard first, then confirm it holds in both.

Team athletes get their team's accent in place of Finish-Line Red, with team-specific ink. This is the only colour swap in the system. Team logos sit on a white tile.

The public pages follow the visitor's device: join defaults dark and privacy defaults light, each switching with `prefers-color-scheme` to the Scoreboard or Daylight values.

### Named Rules
**The One Accent Rule.** Each screen has a single accent colour: Finish-Line Red, or the team's accent when one applies. Never add a second brand colour.

**The Fill And Text Rule.** A colour used as a fill and as text needs both roles to pass 4.5:1. Use accent or rest for fills and accent-text or blue for text.

**The Colour Means Status Rule.** Green, amber and blue always carry their meaning. Never use them to decorate.

## Typography

**Display Font:** Barlow Condensed (with Arial Narrow, Helvetica Neue, Arial)
**Body Font:** Barlow (with Helvetica Neue, Arial)

**Character:** Barlow Condensed has the narrow, tall stance of a scoreboard numeral. Barlow is the same family at reading width, so numbers and sentences feel related without competing.

### Hierarchy
- **Display** (800, 92px, 0.82): The week number on Today only. Drops to 76px below 370px wide. Other big result numbers (56px finish panel, 34px rest clock, 32px stats) use the same weight and tight leading.
- **Headline** (800, 44px, 1.02, uppercase): Page titles. Public pages use `clamp(40px, 9vw, 60px)`.
- **Title** (700, 24px, 1.02, uppercase): Section headings. Exercise and card titles run 20 to 22px in the same style.
- **Body** (400, 16px, 1.45): All reading text. Secondary text runs 13 to 14px. Long text stops at 62 to 65ch.
- **Label** (700, 13px, 0.12em, uppercase): Eyebrows, field labels, tabs and status tags, from 11px to 15px with 0.06 to 0.12em tracking.

### Named Rules
**The Tabular Numbers Rule.** Every number that changes or lines up in a column uses tabular figures.

**The Two Voices Rule.** Condensed uppercase labels and counts. Barlow explains. Never set a sentence in uppercase condensed type.

## Layout

One centred column, 540px at most, with side gutters of at least 16px that respect the phone's safe areas. The top bar is sticky, the five-tab bar is fixed to the bottom, and the rest timer docks just above the tabs. Sections stack with 12px inner gaps and 18px of vertical padding. Cards use 14 to 16px of padding, and lists use 6 to 8px gaps.

Grids are fixed to their content rather than fluid: the set row has five columns (28px, flexible, 74px, 62px, 46px) and tightens below 370px. The stats row is three equal cells. Public pages widen to 720px (join) and 640px (privacy), and the three plan cards stack below 620px.

Overlays rise as bottom sheets, within the thumb's reach, capped at 88% of the screen height.

## Elevation & Depth

Flat by default. Depth comes from three tonal steps (Scoreboard Black, Panel Charcoal, Raised Graphite) and a 1px Hairline border. Shadows appear only on things that float over content.

### Shadow Vocabulary
- **Floating panel** (`box-shadow: 0 10px 30px rgba(0,0,0,.35)`): The rest timer.
- **Toast** (`box-shadow: 0 8px 24px rgba(0,0,0,.3)`): Brief confirmations.

### Named Rules
**The Flat-And-Firm Rule.** Cards and buttons never cast a shadow at rest. If it does not float over content, it stays flat. Selection is shown with a border or a 1px ring, not with lift.

## Shapes

Gently rounded and consistent, tightening as elements get smaller: cards at 14px, buttons and list rows at 12px, inputs at 10px, chips and tags at 6px, sheet tops at 20px. Fully round shapes are reserved for pills, dots, avatars and pips. Week cells and progress bars keep small radii so they read as lit segments.

## Components

### Buttons
Solid and confident.
- **Shape:** Firmly rounded (12px).
- **Primary:** Finish-Line Red with Button White text in condensed 800 at 18px, tracked and uppercase. Often full width.
- **Ghost:** Raised Graphite with Cream text and a Hairline border, for secondary actions.
- **Focus:** A 2px Signal Blue outline with a 2px offset across the app.
- **Hover:** None in the app, which is touch-only. Join's language toggle brightens its text on hover.

### Chips
- **Style:** Raised Graphite with Weathered Grey text and a Hairline border, 12px semibold.
- **Phase pill:** Fully round and condensed, with a red dot.
- **Status tag:** Outlined by default, amber outline for partly done, solid Result Green with Green Ink when done.

### Cards / Containers
- **Corner Style:** 14px.
- **Background:** Panel Charcoal.
- **Shadow Strategy:** None, per the Flat-And-Firm Rule.
- **Border:** 1px Hairline, switching to Finish-Line Red for the current or featured item.
- **Internal Padding:** 14 to 16px, 20px on public pages.

### Inputs / Fields
- **Style:** Raised Graphite with a Hairline border, 10px radius, 44 to 46px tall. Set inputs are centred, semibold, tabular 18px.
- **Focus:** The shared Signal Blue outline.
- **Error / Warning:** Amber border with a soft amber ring.
- **Done:** A green-tinted border on the finished set row.

### Navigation
- **Style:** Five equal tabs with a 22px icon above a 12px condensed uppercase label, on Panel Charcoal with a Hairline top border.
- **Inactive:** Dim Grey.
- **Active:** Cream label with a Finish-Line Red icon.
- **Top bar:** Team logo or DB Speed seal, with name and sync status, on Scoreboard Black.

### Season Bar
The scoreboard signature: 32 thin cells, one per week, coloured by training phase. Past weeks dim to 55% and the current week gets a Cream outline. It sits under the giant week number.

### Rest Timer
A docked Rest Blue bar above the tabs with a large tabular clock, turning Result Green when rest is over. It is one of only two elements that casts a shadow.

### Benchmark Ladder
Stacked rows from Entry to NT Strong, each with a label, a bar and a value. Bars are Dim Grey by default, Result Green once hit, and Target Amber for the next rung.

### Set Row
The core logging control: set number, target, weight, reps and a 44px check button. Ticking the check fills it Result Green.

## Do's and Don'ts

### Do:
- **Do** make the number the largest thing on any screen that has a key number.
- **Do** keep all text contrast at 4.5:1 or better, in all three skins and with team accents, and tap targets at 44px or larger.
- **Do** keep every app screen within the 540px single column.
- **Do** use the stylesheet's colour variables, so skins and team accents keep working.
- **Do** check new work in French too, since it runs longer in uppercase condensed labels.
- **Do** switch off motion for people who ask for reduced motion, as the app does today.

### Don't:
- **Don't** add a second accent colour or use status colours as decoration.
- **Don't** put shadows on cards or buttons.
- **Don't** use a font other than Barlow and Barlow Condensed.
- **Don't** make Lake or Daylight the design reference. Scoreboard is the system.
- **Don't** add a colour swap other than the team accent.
- **Don't** dim text with opacity. Show locked or past items with Weathered Grey instead.

## Known Debts

Measured against the floors in PRODUCT.md. These describe the current code, not the target. Fix them in a design change rather than copying them into new work.

- Some controls are under 44px: the avatar (36px), the settings segments (42px), the switch (30px), and the Demo and Back controls.
- Join uses slightly different Hairline (#2c2f34) and Raised (#23262a) values from the app.
- The privacy page still uses the old red (#e5482b) for links, which is 4.26:1 on its dark cards.
- The logo and the skin swatches in settings still use the old red (#e5482b), set in JavaScript. Neither is text.
