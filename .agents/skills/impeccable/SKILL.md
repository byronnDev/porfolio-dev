---
name: impeccable
description: "Design, implement or review frontend interfaces for usability, accessibility and visual quality. Not for backend or non-UI tasks."
---

# Impeccable

Design and improve the requested interface using the project's existing identity,
components and platform. Read the affected UI and the design/product context needed
for the current decision. Missing PRODUCT.md or DESIGN.md is not a blocker to a scoped
edit, and does not authorize an onboarding interview or unrelated configuration changes.

## Outcomes and boundaries

- Preserve accessibility: readable contrast, labels, keyboard/focus behavior, usable
  touch targets and reduced motion. Keep content visible if animation fails.
- Preserve the user's brief and established design system. Style examples, palette
  suggestions and anti-pattern catalogs are heuristics, not universal bans or reasons
  to override an explicitly requested appearance.
- For implementation, continue through rendering/interaction checks and fixes in scope.
  For a critique, return findings. Do not turn either into a multi-stage design approval
  process unless the user requested guided exploration or left a material choice open.
- Use native-platform equivalents for native apps; browser/CSS recipes apply to web
  views. A web preview does not validate native behavior.

## Reference routing

Read only the reference for an explicitly named command or a substantial workflow
that needs it. Ordinary spacing, copy or component edits can proceed directly.
For a new design direction, use [brand](reference/brand.md) for marketing or
[product](reference/product.md) for app interfaces, according to the target surface.
The requested deliverable and existing authorization determine review gates in those
workflows; ask only for unresolved consequential choices. Detailed live-mode security,
CSP and manual-edit consent requirements remain scoped to live mode.

Use `init` only for requested project-context setup. `shape` is planning-only when
requested; a request to build does not require stopping after a shape draft.
The context/palette scripts are optional aids when the task needs them. Do not follow
an update/setup suggestion by modifying installed tooling outside the task.

## Commands

| Command | Category | Description | Reference |
|---|---|---|---|
| `craft [feature]` | Build | Shape, then build a feature end-to-end | [reference/craft.md](reference/craft.md) |
| `shape [feature]` | Build | Plan UX/UI before writing code | [reference/shape.md](reference/shape.md) |
| `init` | Build | Set up project context: PRODUCT.md, DESIGN.md, live config, next steps | [reference/init.md](reference/init.md) |
| `document` | Build | Generate DESIGN.md from existing project code | [reference/document.md](reference/document.md) |
| `extract [target]` | Build | Pull reusable tokens and components into design system | [reference/extract.md](reference/extract.md) |
| `critique [target]` | Evaluate | UX design review with heuristic scoring | [reference/critique.md](reference/critique.md) |
| `audit [target]` | Evaluate | Technical quality checks (a11y, perf, responsive) | [reference/audit.md](reference/audit.md) |
| `polish [target]` | Refine | Final quality pass before shipping | [reference/polish.md](reference/polish.md) |
| `bolder [target]` | Refine | Amplify safe or bland designs | [reference/bolder.md](reference/bolder.md) |
| `quieter [target]` | Refine | Tone down aggressive or overstimulating designs | [reference/quieter.md](reference/quieter.md) |
| `distill [target]` | Refine | Strip to essence, remove complexity | [reference/distill.md](reference/distill.md) |
| `harden [target]` | Refine | Production-ready: errors, i18n, edge cases | [reference/harden.md](reference/harden.md) |
| `onboard [target]` | Refine | Design first-run flows, empty states, activation | [reference/onboard.md](reference/onboard.md) |
| `animate [target]` | Enhance | Add purposeful animations and motion | [reference/animate.md](reference/animate.md) |
| `colorize [target]` | Enhance | Add strategic color to monochromatic UIs | [reference/colorize.md](reference/colorize.md) |
| `typeset [target]` | Enhance | Improve typography hierarchy and fonts | [reference/typeset.md](reference/typeset.md) |
| `layout [target]` | Enhance | Fix spacing, rhythm, and visual hierarchy | [reference/layout.md](reference/layout.md) |
| `delight [target]` | Enhance | Add personality and memorable touches | [reference/delight.md](reference/delight.md) |
| `overdrive [target]` | Enhance | Push past conventional limits | [reference/overdrive.md](reference/overdrive.md) |
| `clarify [target]` | Fix | Improve UX copy, labels, and error messages | [reference/clarify.md](reference/clarify.md) |
| `adapt [target]` | Fix | Adapt for different devices and screen sizes | [reference/adapt.md](reference/adapt.md) |
| `optimize [target]` | Fix | Diagnose and fix UI performance | [reference/optimize.md](reference/optimize.md) |
| `live` | Iterate | Visual variant mode: pick elements in the browser, generate alternatives | [reference/live.md](reference/live.md) |

Plus two management commands: `pin <command>` and `unpin <command>`, described below.


## Management commands

For an explicit pin/unpin request, run `node .agents/skills/impeccable/scripts/pin.mjs <pin|unpin> <command>`.
This writes shortcuts across detected harness directories; inspect the resulting diff.
For a bare skill invocation without a task, offer relevant commands instead of making
unrequested edits. Choose routine implementation details from existing evidence;
ask only if the desired outcome cannot be inferred.
