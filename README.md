# Case study builder (Behance)

A Claude skill that turns app screens, a logo and a design guide into a structured, Behance-ready UX case study. It handles the section order, copy rules, layout tokens, PNG and PDF export, and a pre-publish checklist.

## What it does

- Asks for missing inputs first (logo, screens, design guide, project facts) instead of guessing.
- Builds 19 sections in a fixed order, from cover to closing page, each as a separate 1400px segment.
- Exports each segment as a numbered 2x PNG, plus a PDF and a self-contained HTML file.
- Blocks invented data: missing metrics are left out, and "tested with one person" is never written as a sample size.

## Install

1. Download `behance-case-study-builder/SKILL.md` from this repo.
2. Add it to Claude as a skill (Settings, then Skills, then upload or create from file).
3. Optional: install the recommended skills listed in section 7 of `SKILL.md` (`minimalist-ui`, `frontend-design`, `ux-writing`, `design-critique`).

## How to use

Open a new chat with the skill enabled and say what you have, for example:

> Build a Behance case study for [app name]. I have the screens, the logo and the design guide. Start with intake.

Claude will ask for anything missing before it writes any section copy.

## Files

- `behance-case-study-builder/SKILL.md`: the skill itself (intake rules, section order, writing rules, layout tokens, export steps, pre-publish checklist).

## Notes

- Screens, photos and logos are not included. Bring your own.
- Check photo rights and consent before publishing, and confirm clinical or safety copy has been reviewed.
