# Case study builder

A Claude skill that turns app screens, a logo and a design guide into a Behance-ready UX case study: section order, copy rules, layout tokens, and PNG, PDF and HTML export.

## Install

1. Unzip the download. SKILL.md sits at the top level.
2. Add the skill in Claude (Settings, then Skills, then upload).
3. Optional: install the recommended skills listed at the end of SKILL.md.

## Try it

> Build a Behance case study for [app name]. I have the screens, the logo and the design guide. Start with intake.

Claude asks for anything missing before writing copy.

## Test plan

Expected inputs and outputs for checking the skill works:

| Test | Input | Expected |
| --- | --- | --- |
| Trigger | "Build a Behance case study for my app" | Skill activates, starts intake |
| Trigger | "Turn my app screens into a case study" | Skill activates |
| No-trigger | "Make me a slide deck" | Skill does not activate |
| Missing data | Brief with no tester count | Output says the count is missing, no number invented |
| Placeholder check | Any finished run | No square-bracket placeholders in output |
| Export | Finished HTML | 19 numbered PNGs at 2800px wide, PDF with one segment per page |

## Files

- `SKILL.md`: the skill.
- `examples/sample-intake.md`: a filled intake and the segment order it produces.

## Notes

- Screens, photos and logos are not included. Bring your own.
- Confirm photo rights and consent before publishing, and confirm clinical or safety copy has been reviewed.
