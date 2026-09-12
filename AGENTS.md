# mikeldev.com agent guide

Astro portfolio with Tailwind, GSAP and a server-side Resend contact endpoint.
Use pnpm and the `packageManager` pin in `package.json`. Deployment configuration is
in `astro.config.mjs` and `wrangler.jsonc`; do not infer it from older README badges.

## Task context

- For layout or branding, use the affected Astro page/components, shared styles and
  `PRODUCT.md` where it informs the requested design decision.
- For contact delivery, inspect the existing endpoint and `.env.example`; preserve
  server-side validation, escaped user content and private credentials.
- Load `.agents/skills/impeccable` for design work, `resend` for SDK/API work and
  `resend-cli` for terminal operations. `react-email` applies only to React Email
  templates/editor work; it is not a reason to migrate direct HTML emails.
- Prefer existing components and native features; keep changes scoped to the task.

## Decisions and completion

Resolve routine, reversible choices from the task and repository evidence; state only
assumptions that materially affect the result. Ask when missing information changes
the product outcome, public contract, data safety or authorization and cannot be inferred.
Continue implementation, relevant verification and fixes caused by the change until
the requested outcome is complete. A first draft is not a review gate unless requested.

Local edits, focused checks and scoped fixes need no repeated approval. Remote writes,
sends, deployments, destructive operations and credential changes must be within the
user's authorization for the named target; ask only for missing authorization. Permission
to commit or push does not also authorize deployment or unrelated changes.
Preserve unrelated user work and do not bypass hooks or force-push.

## Validation and commits

For documentation-only changes, review claims and links and run `git diff --check`.
For code, select checks for the affected behavior and risk. A passing combined gate
covers its constituent checks; rerun only after relevant changes or to investigate a
failure. Report checks actually run and any blocker; do not call skipped checks passed.

`pnpm test` runs the Node tests. `pnpm build` includes those tests, Astro checks and
the build. Use `pnpm check` for Astro diagnostics and targeted Prettier checks for
formatting. `pnpm verify:agents` is a public-site/API readiness check, not a validator
for these instruction files; inspect its target before running it.

Use atomic Conventional Commits in English. Versioned Husky hooks format staged files
with `pnpm lint-staged`, validate messages with Commitlint, and run `pnpm build` before
push. Respect configured hooks; when delivering from a fresh checkout, install with
`pnpm install --frozen-lockfile` to activate them.
