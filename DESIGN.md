---
name: "Together, Apart."
description: "Exhibition catalogue — spacious, visual and presentation-led."
colors:
  primary: "#994f39"
  ivory: "#f8f6f0"
  ink: "#282823"
  rule: "#c8c3b8"
  tonal-ground: "#eae5d9"
  on-primary: "#ffffff"
  muted-ink: "#56574e"
  strategy-define: "#a95d46"
  strategy-extend: "#687f70"
  strategy-mediate: "#516f8c"
  annotation-clay: "#994f39"
  annotation-sage: "#526b59"
typography:
  display:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "clamp(3.5rem, 7vw, 6rem)"
    fontWeight: 700
    lineHeight: 0.9
    letterSpacing: "-0.04em"
  chapter-display:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "clamp(2.75rem, 5.6vw, 6rem)"
    fontWeight: 700
    lineHeight: 0.98
    letterSpacing: "-0.06em"
  body:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  reading-body:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.75
  source-title:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "1.15rem"
    fontWeight: 700
    lineHeight: 1.4
    letterSpacing: "-0.02em"
  label:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "12px"
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: "0.07em"
  action:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 600
  research-action:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 400
  field:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "0.83rem"
    fontWeight: 600
  navigation:
    fontFamily: "Montserrat, \"Helvetica Neue\", Arial, sans-serif"
    fontSize: "0.9rem"
    fontWeight: 400
rounded:
  square: "0px"
spacing:
  control-gap: "0.75rem"
  stack: "1rem"
  panel-gap: "20px"
  home-gutter: "clamp(18px, 2.6vw, 46px)"
  reader-gap: "clamp(2rem, 4vw, 4rem)"
  reader-section: "clamp(2.5rem, 5vw, 4rem)"
  site-gap: "clamp(1.5rem, 3vw, 3rem)"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.action}"
    rounded: "{rounded.square}"
    padding: "10px 18px"
  button-secondary:
    backgroundColor: "{colors.ivory}"
    textColor: "{colors.primary}"
    typography: "{typography.action}"
    rounded: "{rounded.square}"
    padding: "10px 18px"
  button-secondary-hover:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
  research-action:
    backgroundColor: "{colors.ivory}"
    textColor: "{colors.primary}"
    typography: "{typography.research-action}"
    rounded: "{rounded.square}"
    padding: "0.6rem 0.8rem"
  search-field:
    backgroundColor: "{colors.ivory}"
    textColor: "{colors.ink}"
    typography: "{typography.field}"
    rounded: "{rounded.square}"
    padding: "0.5rem 0.75rem"
    width: "100%"
  main-navigation:
    textColor: "{colors.ink}"
    typography: "{typography.navigation}"
    rounded: "{rounded.square}"
    padding: "0.5rem 0.2rem"
  filter-chip:
    backgroundColor: "{colors.ivory}"
    textColor: "{colors.primary}"
    rounded: "{rounded.square}"
    padding: "0.4rem 0.65rem"
  chapter-panel:
    backgroundColor: "{colors.ivory}"
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    padding: "20px clamp(18px, 2.6vw, 46px) 28px"
  matching-source:
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    padding: "1.25rem 0"
  dwelling-study:
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    padding: "1rem 0 0"
  research-preview:
    backgroundColor: "rgba(248,246,240,.96)"
    textColor: "{colors.ink}"
    rounded: "{rounded.square}"
    padding: "0.85rem 1rem"
---

# Design System: Together, Apart.

## Overview

**Creative North Star: "Exhibition catalogue"**

Together, Apart. is presented as an exhibition catalogue: spacious, visual and presentation-led. Architectural drawings and supplied project images carry the work; clear typography, warm surfaces and fine rules organise its reading.

Controls are restrained and precise. Square edges, fine borders and explicit interaction states give the site a consistent frame. Depth is lightly layered where separation is useful, with the existing research preview providing the model for a subtle contextual shadow.

**Key Characteristics:**

- Spacious compositions with a clear reading hierarchy.
- Clay, ivory and ink, with separate colours for recorded research relationships.
- Square panels and controls, fine rules and visible keyboard focus.
- Supplied drawings kept legible, proportional and available at full size.

This document records the implementation on the review branch at commit `75fed6594dd15a8fd648eca681e3b5e5ce36be09`, checked on 17 November 2026. Sources are `atlas.css`, the later exegesis-specific `exegesis/layout.css`, and current page markup. This is the review implementation, not a claim that it is deployed. It combines the implemented system with Adam's confirmed descriptive direction. It does not change the interface. Frontmatter names are documentation aliases for existing variables and repeated values; they do not imply an installed token library.

## Colors

The main palette is clay, ivory and ink. Research colours identify recorded relationships and do not replace the main action colour. Generated tonal ramps in the companion file are preview aids, not additional colours shipped by the website.

### Primary

- **Clay** (`primary`): links, primary actions, selected states, chapter numbers and limited emphasis.
- **White on clay** (`on-primary`): text inside filled Home actions.

### Secondary

- **DEFINE clay**, **EXTEND sage** and **MEDIATE slate** (`strategy-define`, `strategy-extend`, `strategy-mediate`): the three strategy colours used in the research network. The chart also has an existing categorical palette in its script; preserve those assignments when extending the chart.

Annotation text uses **Annotation clay** and **Annotation sage** (`annotation-clay`, `annotation-sage`) on ivory. These darker text variants preserve the original strategy colours in drawings and the research network. Their measured contrast against ivory is 5.50:1 and 5.39:1 respectively.

### Neutral

- **Ivory** (`ivory`): the page ground and ordinary control surfaces.
- **Ink** (`ink`): headings, body text and strong boundaries.
- **Fine rule** (`rule`): panel edges, separators and input borders.
- **Tonal ground** (`tonal-ground`): selected-source backgrounds and quiet secondary areas.
- **Muted ink** (`muted-ink`): supporting metadata and notes.

**The Drawing Integrity Rule.** Preserve the complete proportions, annotations and colours of supplied drawings. Use supplied artwork; omit unavailable media rather than publishing an empty image slot.

**The Visible Choice Rule.** Pair colour with text, an underline, a border or a pressed state. Keep active filters visible and removable.

## Typography

Montserrat is self-hosted from `assets/fonts/montserrat-latin.woff`, with Helvetica Neue, Arial and sans-serif fallbacks. The font declaration spans weights 100–900 with font-display swap. Labels use the same family; there is no separate implemented monospace face.

- **Display:** the Home title uses the `display` token. On screens up to 720 px it uses `clamp(3.5rem, 13vw, 5.5rem)`.
- **Chapter display:** chapter titles use `chapter-display`, usually uppercase. Its tighter tracking is an existing implementation value, distinct from Home.
- **Body:** ordinary paragraphs use `body`; long manuscript paragraphs use `reading-body` and a measure of 68 characters. Other journal pages retain their 64-character base measure.
- **Chapter hierarchy:** use one H1, section H2s and nested H3s. Section titles use `clamp(1.35rem, 2vw, 2rem)` with a 1.2 line height; subsection roles retain their existing sizes, including larger precedent and journal-study titles. At 820 px and below, chapter display uses `clamp(2.25rem, 9.5vw, 4rem)`.
- **Source title:** matching-result headings use `source-title`, with an underlined link.
- **Label:** Home chapter numbers use `label`, uppercase with tabular numerals. Figure labels are smaller (0.72 rem), while figure-caption prose is 0.78 rem with a 1.5 line height.
- **Controls:** use the action, research-action, field and navigation roles for their respective components. Avoid applying display tracking to control labels.

## Layout

The site uses fluid grids and constrained reading measures. Spacing values in the frontmatter capture recurring implemented values, rather than a universal mathematical scale.

- **Home:** full-width composition; a two-column hero places an opaque text area beside the render. At 720 px and below the image and text stack. Six chapter panels use three columns, two at 900 px and below, and one at 600 px and below.
- **Reading pages:** the current container is the smaller of 91% and 88 rem. A sticky contents rail sits beside the manuscript. At 820 px and below it becomes a compact expandable index and the manuscript becomes a single column. The exegesis rail is 11 rem wide, reducing to 10 rem at 1000 px. Prose stays in one aligned reading column, with figures spanning the manuscript field. Precedent images and commentary pair above 1000 px and stack below. Contents use two columns, becoming one at 650 px.
- **Research:** the network and chart sit alongside one another above 1050 px; below that they stack. At 820 px and below, or with a coarse pointer, the graph starts collapsed. Search and the matching-source list remain available.
- **Data centre:** heat-recovery steps use numbered rows with separate number, title and explanation columns; below 820 px the explanation sits beneath its title. Metrics and energy-balance groups stack below 480 px. Shared section rhythm uses `reader-section`; Home panel spacing uses `site-gap`.
- **Fields:** flexible labels and controls permit shrinking; inputs and selects fill their available width. At 420 px and below each network control occupies a complete row.
- **Matching sources:** desktop rows separate number, title/finding and action. At 820 px and below they stack. Show twelve results initially and reveal twelve more per action.
- **Drawings:** fit complete figures within the available width. Manuscript images use automatic height and full-size links. Home render cropping is separate from drawing placement.

Maintain a minimum 44 px height for the implemented main navigation, network fields, filter chips and research actions. This does not imply that every graph point meets that target.

## Elevation & Depth

Light layering is selective. Chapter panels, fields and buttons have no shadow. Fine rules, spacing and tonal backgrounds separate ordinary content.

The desktop research preview uses the existing shadow `0 8px 24px rgba(40,40,35,.12)`, a nearly opaque ivory surface and a fine border. Its role is to distinguish a temporary preview from the network beneath. It is hidden on compact/coarse-pointer layouts.

**The Selective Layering Rule.** Keep ordinary controls and content panels flat. Reserve subtle shadows for contextual elements that need separation from the content beneath.

The current Home panel transition changes border colour over 180 ms with ease timing. Reduced-motion preferences remove it. Network motion is finite, pauses when hidden or out of view, and uses a non-animated settling path for reduced motion.

## Shapes

Panels, buttons, chips and fields have square corners. Thin rectangular boundaries form the ordinary interface language; circles belong to the research graph and pie chart.

Use a one-pixel rule for ordinary edges. Keep graph strokes, selected outlines and the existing evidence markers distinct from general container borders. Filter chips are rectangular controls, not pills.

## Components

### Buttons

Home primary actions use clay with white text; secondary actions use an ivory ground, clay text and a clay border. Secondary hover becomes filled. Both use the square shape and action padding from the frontmatter.

Research actions are smaller text controls with fine borders and a minimum 44 px height. Focus uses a visible clay outline. Primary hover and action active states use ink with ivory text.

### Chips

Active-filter chips name the search, tag, strategy, chart, matrix or keyword selection. Each chip removes that selection, exposes an accessible removal label, wraps long text and retains its rectangular border.

The ALL/ANY control appears when at least two network selections need combining.

### Cards / Containers

Home chapter panels are single keyboard-accessible links with a chapter number, supplied image with attribution where needed, title and introduction. Their default shadow is none. Hover changes the border and heading colour; focus outlines the complete link.

Keep supplied images proportional and retain source credits. Do not add empty image slots or substitute instructional PNGs. The sidecar chapter specimen uses a real project asset.

### Inputs / Fields

Use visible labels, native search fields and native selects. Fields have an ivory background, ink text, fine border and square corners. Prevent long select options from widening the page.

Keep loading, retry and no-match feedback readable. Missing recorded research remains explicitly missing.

### Navigation

The masthead uses the name at the left and main links at the right. The current page has a clay underline as well as colour. At 820 px and below, the six links collapse into the Menu disclosure beneath the name (verify the exact breakpoint behaviour in `atlas.css`), retaining 44 px minimum link heights.

Reading pages use a sticky contents rail with a compact toggle, Escape dismissal and a current-section label. Keep the skip-to-content and skip-to-matching-sources links.

### Matching sources and full register

Matching results show a point number, title, finding and Show in network action. A title link opens the corresponding full entry. The complete register remains separately available in display-number order.

Filter state is restored from the URL. Direct source hashes open the relevant entry after the dataset loads.

### Research network and preview

Selecting a point inspects its finding; Explore related points is a separate action based on shared relevance or strategy tags. Selecting a hub filters by its tag.

The graph has one sequential keyboard stop; arrow keys move between its points and tags. Enter or Space activates the focused item. Desktop supports dragging and previews. Compact layouts allow vertical scrolling over points and omit hover previews.

### Dwelling comparisons

Home presents Stacked homes, Side-by-side homes and XL dwelling together as three ruled columns, each with a supplied plan, description and Proposal link. At 760 px and below, the region scrolls horizontally with 85%-width items, proximity snapping and a visible scroll hint. Preserve the complete drawings within their square display fields. These are comparison articles, not accordions.

## Do's and Don'ts

### Do

- Do lead with supplied project imagery and a clear hierarchy.
- Do keep clay for actions and emphasis, ivory for the ground, and ink for reading.
- Do preserve square controls, fine rules and visible focus.
- Do retain both matching research results and the complete source register.
- Do check narrow layouts against long labels and real findings.

### Don't

- Don't generate substitute drawings, add empty image slots or publish placeholder-instruction images.
- Don't use shadows on every panel or introduce rounded cards as the default.
- Don't communicate selection through colour alone.
- Don't make a graph the only route to reading research.
- Don't reintroduce the removed prototype CSS or `atlas.js`; the active Research implementation is `atlas-research.js`.
