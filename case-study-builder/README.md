# Case study builder

A Claude skill that turns app screens, a logo and a design guide into a UX or product design case study for a portfolio website, Behance, Dribbble or a PDF. It covers section order, copy rules, layout tokens, and numbered image, PDF and HTML export.

## Install

1. Unzip the download. SKILL.md sits inside the case-study-builder folder.
2. Add the skill in Claude (Settings, then Skills, then upload).
3. Optional: install the recommended skills listed at the end of SKILL.md.

## Try it

> Build a case study for my app for my portfolio site and Dribbble. I have the screens, the logo and the design guide. Start with intake.

Claude asks for anything missing, including which platforms you're publishing to, before it writes any copy.

## Test plan

Expected inputs and outputs for checking the skill works:

| Test | Input | Expected |
| --- | --- | --- |
| Trigger | "Build a case study for my portfolio" | Skill activates, starts intake |
| Trigger | "Make a Behance case study" | Skill activates |
| No-trigger | "Make me a slide deck" | Skill does not activate |
| Missing data | Brief with no testing details | Output says testing details are missing, no number invented |
| Placeholder check | Any finished run | No square-bracket placeholders in output |
| Export | Finished HTML | Numbered 2x PNGs in order, PDF with one segment per page |

## Files

- `SKILL.md`: the skill.
- `examples/sample-intake.md`: a fictional filled intake and the segment order it produces.

## Notes

- Screens, photos and logos are not included. Bring your own.
- Confirm photo rights and consent before publishing, and confirm clinical or safety copy has been reviewed.
