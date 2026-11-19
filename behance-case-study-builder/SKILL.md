---
name: behance-case-study-builder
description: Use when the user asks to build a Behance case study, a portfolio case study, or a UX case study PDF from app screens, a logo and a design guide. Trigger phrases include "build a Behance case study", "turn my app screens into a case study", "export my case study as numbered PNG segments". Produces segment layouts, section copy, and PNG, PDF and HTML export. Do not use for a single slide, a one-off social post, or a case study with no screens.
---

# Behance case study builder

## Scope

Do NOT use for: a single slide or social post, a Figma file build, or a case study with no screens (ask for the screens first).

## Input and output

**Input:** app screens (PNG or WebP, one file per screen), a logo (SVG or transparent PNG), a design guide (colours, typeface, type sizes, radius, spacing, icon style), and project facts (role, tools, dates, testing, status).

**Output:** a numbered set of 2x PNG segments in document order, a PDF with one segment per page, and a self-contained HTML source. Deliver them as one zip named after the project.

## Steps

1. **Intake.** Ask for anything missing (see the list below). Do not start building until the required inputs are in.
2. **Check facts.** Use only facts the person gives you. Flag any claim with no source and ask whether it can be backed up or softened.
3. **Plan the structure.** Choose the sections from the list below. Skip a section only if the material does not exist, and say so.
4. **Write the copy.** Follow the writing rules. Every decision explains why it was made.
5. **Build the HTML.** One `<section class="seg" data-name="NN-name">` per section, 1400px wide, with screens and photos referenced by relative path.
6. **Export.** Render each segment as PNG at 2x (2800px wide). Keep numbering in document order (01-cover, 02-overview, and so on). Make the PDF and the self-contained HTML.
7. **Run the pre-publish check** (section 6 below) and report anything that failed.

## Intake (ask before building)

- Logo: SVG preferred, otherwise a transparent PNG. Mark only, or mark plus wordmark?
- Screens: every flow, plus the lock screen, home, and any error or empty states.
- Design guide: colour hex values with roles, the app typeface, type sizes, radius, spacing, icon style.
- Project facts: role, tools, dates (month and year), who tested it and how many people, what they said, what was not tested, status (concept, prototype, shipped).
- Photos: are they real people, and is the person consented or the image licensed?

## Structure (segments, in this order)

1. **Cover:** header image or hero screen, project name, field, and a centred chip row (role, tools, testing status, month and year).
2. **Overview:** one-sentence headline; stat cards for screens and key decisions; role, tools, testing, status.
3. **Problem:** a headline that states the problem; a simple diagram of where the existing experience stops; one line each on what the user and the other stakeholder (for example, a caregiver) need.
4. **Persona:** name, age, role, goals, frustrations, needs. Mark it as illustrative.
5. **Testing:** sample size, what was helpful, what was not tested, next steps.
6. **Process:** the real steps in order, each with a one-line result.
7. **Structure:** navigation (tabs, entry points), with the central action called out.
8. **In use:** three to four real screens in context, with short labels.
9. **Brand in context:** photos of the product in use, plus one colour-rule card.
10. **Flow:** a map of the screens, grouped under the entry points.
11. **Decisions** (usually 3 to 5, one segment each): headline; screens; Why; Trade-off; Alternative considered (if one exists); Status (tested or not).
12. **Accessibility:** the settings that change the app, with contrast ratios computed, not estimated.
13. **Typography and colour:** the app typeface specimen, type scale, swatches with roles.
14. **Design system:** colour roles, type scale, radius, spacing, icons, contrast table.
15. **Components:** buttons, chips, status pills, cards, tab bar, toggles, progress, each shown on real screens.
16. **Low fidelity:** the flow in greyscale, labelled.
17. **High fidelity:** one segment per group, each with a label pill, a one-line description, and captioned screens.
18. **Outcome:** what is known (only what was tested), what is next (dated only if known), what was learned.
19. **Closing page:** full-bleed image with a white fade, "Thanks for scrolling", the logo in one corner, and "UX design by [name]" in the other.

## Writing rules

- Plain English, short sentences, no em dashes (use commas, full stops, or colons).
- Headlines state the point. Labels are one or two words.
- Captions name the screen and its state, and match the screen.
- Do not describe features that do not appear in the screens.
- Clinical, medical or safety copy needs a status line saying whether it has been clinically reviewed.

## Layout and visual rules

- Segment width 1400px, side padding 96px, card padding 32px, bento gap 20px, six columns.
- Type: display 56px for section headlines, 24px for card titles, body 16px, small 13px, label 11px uppercase with 0.12em tracking.
- Colour: palette as tokens with roles. One accent for actions, one alert colour reserved for emergencies, neutrals for the rest. Compute contrast for every text pair you claim is accessible.
- Phone frames: white outline, outer radius about 52px, screen radius about 40px, height auto so no screen is cropped.
- Low fidelity: `grayscale(100%)` on screenshots only.
- Logo: keep transparency. If it has a white background, place it on a white card.

## Boundaries

- Never invent metrics, sample sizes, dates, quotes or testers. Leave missing items out and say so.
- Never write placeholder text such as "[Add dates]" in final output.
- Label illustrative personas as illustrative, not measured.
- If one person tested the design, say "tested with one person".
- Never embed API keys, tokens or personal contact details in any output file.

## Pre-publish check

- No placeholder text (search for square brackets and "Add").
- Every caption matches its screen.
- Every claim has a source or is marked as the designer's view.
- Photo rights and consent confirmed; logo is the official asset.
- Chips and footer are centred and aligned; every image is sharp at 100% zoom.

## Examples

See `examples/sample-intake.md` for a filled intake and the segment order it produces.

## Recommended skills

For a sleeker result, install these first if available: `minimalist-ui` (spacing, type, colour), `frontend-design` (segment composition), `ux-writing` (section copy), `design-critique` (review each segment before export). If any are missing, continue with the rules above.
