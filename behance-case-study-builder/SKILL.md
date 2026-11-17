---
name: "behance-case-study-builder"
description: "Build a structured, Behance-ready UX case study from app screens, a logo and a design guide: segment layout, section copy, PNG and PDF export."
---

# Behance case study builder

Use this skill when someone gives you app screens, a logo and a design guide and wants a portfolio case study for Behance (or a PDF of the same). Follow the order below. Do not skip intake, and do not invent data.

## 1. Intake (ask before building)

Ask for anything missing. Do not guess these:
- Logo: SVG preferred, otherwise a transparent PNG. Ask whether it is mark only or mark plus wordmark.
- Screens: exported PNG or WebP, one file per screen, with clear names. Ask for the lock screen, home, every flow, and any error or empty states.
- Design guide: colour hex values with their roles, the app typeface, type sizes, radius and spacing, and icon style.
- Project facts: role, tools, dates (month and year), who tested it and how many people, what they said, what was not tested, and status (concept, prototype, shipped).
- Photos: whether they are real people, and whether the person is consented or the image is licensed.

Rules for facts:
- Use only facts the person gives you. If a metric is missing, leave it out and say so. Never write a placeholder such as [Add dates] in the final output.
- Label illustrative personas as illustrative, not measured.
- If one person tested the design, say "tested with one person". Do not imply a sample size.
- Flag any claim with no source (for example "most apps stop here") and ask whether it can be backed up or should be softened.

## 2. Structure (segments, in this order)

Build each section as a separate 1400px-wide segment so each exports as one Behance image. Skip a section only if the material does not exist, and say so.

1. **Cover**: header image or hero screen, project name, field, and a chip row: role, tools, testing status, month and year. Chips are centred.
2. **Overview**: one-sentence headline; stat cards for screens designed and key decisions; role, tools, testing, status.
3. **Problem**: headline that states the problem; a simple diagram of where the existing experience stops; the user and the other stakeholder (for example the caregiver) with one line each on what they need.
4. **Persona**: name, age, role, goals, frustrations, needs. Mark as illustrative and built from the test and the problem research.
5. **Testing**: sample size, what was found helpful, what was not tested, next steps.
6. **Process**: the steps taken in order, each with a one-line result. Use only real steps.
7. **Structure**: the navigation (tabs, entry points), with the central action called out.
8. **In use**: three to four real screens in motion or context, with short labels.
9. **Brand in context**: photos of the product in use plus one colour-rule card (for example "blue means act, red means emergency").
10. **Flow**: a mind map of the screens, grouped under the entry points.
11. **Decisions** (one segment each, usually 3 to 5): a headline that states the decision; the screens; "Why" (the reason); "Trade-off" (what it costs); "Alternative considered" if one exists; "Status" (tested or not). Avoid decisions that have no reason written down.
12. **Accessibility**: the settings that change the app (text size, contrast, motion), with contrast ratios computed, not estimated.
13. **Typography and colour**: the app typeface specimen, the type scale, and the colour swatches with roles.
14. **Design system**: colour roles, type scale, radius, spacing, icons, glass if used, contrast table.
15. **Components**: buttons, chips, status pills, cards, tab bar, toggles, progress. Show each as used on real screens.
16. **Low fidelity**: the flow in greyscale (grayscale filter on the screenshots), labelled.
17. **High fidelity**: one segment per group (for example Onboarding, Home, Reminders, How I Feel, Medicines, Caregivers, Profile, Safety). Each segment has a blue pill label with the group name, a one-line description, and each screen with its caption above it.
18. **Outcome**: what is known (only what was tested), what is next (dated only if known), what was learned.
19. **Closing page**: a full-bleed image with a white fade, "Thanks for scrolling", the logo in one corner, and "UX design by [name]" in the other.

## 3. Writing rules

- Plain English. Short sentences. No em dashes (use commas, full stops, or colons).
- Headlines state the point ("Who sees what.", "A missed dose needs a sequence."). Labels are one or two words.
- Every decision explains why it was made, not only what was chosen.
- Captions name the screen and its state ("Empty day", "Step 2: symptoms"). Check captions against the screen.
- Do not describe features that do not appear in the screens.
- Clinical, medical and safety copy needs a status line that says whether it has been clinically reviewed.

## 4. Layout and visual rules

- Segment width 1400px, side padding 96px, card padding 32px, bento grid gap 20px, six columns.
- Headings: display 56px for section headlines, 24px for card titles. Body 16px. Small 13px. Label 11px uppercase with 0.12em tracking. Eyebrow 12px uppercase with a dot.
- Typeface: use the app's typeface in screens and typography specimens. Use a clean sans (for example Inter) for the case study pages if the app font is not suitable for body text. State which one is which.
- Colour: define the palette as tokens with roles. One accent colour for actions only, one alert colour reserved for emergency, neutrals for everything else. Compute contrast for every text pair you claim is accessible.
- Glass cards: white fill fading from about 42% to 12%, backdrop blur about 30px, saturation about 190%, 1px white edge. Keep them light so the background shows.
- Phone frames: white outline, radius about 52px, screen image radius about 40px. Set height to auto so the frame ends where the screen ends. Never crop a screen. Keep all screens in a row the same width.
- Low fidelity: apply grayscale(100%) to screenshots only.
- Photos: crop to the frame with object-fit cover, keep faces in the top third.
- Logo: keep transparency. If the logo has a white background, place it on a white card.

## 5. Build and export

- Build one HTML file with each section as `<section class="seg" data-name="NN-name">`. Reference screens and photos by relative path.
- Export each segment as PNG at 2x device scale (2800px wide). Each PNG should be at least about 1MB. Keep the file numbering in document order (01-cover, 02-overview, and so on).
- Make a self-contained HTML by inlining images as base64 for sharing.
- Make a PDF with one segment per page, in the same order, at full resolution.
- Deliver a zip of the numbered PNGs and the PDF. Name the zip after the project.

## 6. Before publishing (check each item)

- No placeholder text anywhere (search for brackets and "Add").
- Every screen caption matches the screen.
- Every claim has a source or is marked as the designer's view.
- Photo rights and consent are confirmed.
- Logo is the official asset.
- Cover chips and footer are centred and aligned.
- Every image is sharp at 100% zoom.

## 7. Recommended skills to install

For a modern, sleek result, tell the person to install these skills before building:
- `minimalist-ui` for restrained spacing, type and colour.
- `frontend-design` for layout and composition of the HTML segments.
- `ux-writing` for microcopy and section copy.
- `design-critique` to review each segment before export.

If any of these are missing, say so and continue with the rules in this skill.