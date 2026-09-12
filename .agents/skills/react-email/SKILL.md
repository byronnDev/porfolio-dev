---
name: react-email
description: "Create, render or edit React Email templates or its visual editor. Not for sending existing HTML/text through Resend."
license: MIT
metadata:
  author: Resend
  version: "2.1.0"
  homepage: https://react.email
  source: https://github.com/resend/react-email
  openclaw:
    install:
      - kind: node
        package: react-email
        label: React Email
    links:
      repository: https://github.com/resend/react-email
      documentation: https://resend.com/docs/react-email-skill
---

# React Email

Use the installed React Email packages and their version's APIs. This skill does not
imply migrating the portfolio's existing direct HTML/text contact emails to React.
Reuse project branding and assets; infer routine style choices from the brief/code.
Ask only for a missing decision that affects the deliverable or a production asset URL
that cannot be determined. Local previews can proceed while delivery details are pending.

## Template constraints

- Preserve meaningful `lang`, heading structure, alt text, readable contrast and
  a plain-text alternative. Use representative preview props without personal data.
- Prefer email-compatible table/Row/Column layout, pixel dimensions and broadly
  supported image formats; check support for the actual target email clients.
- Use absolute hosted asset URLs for delivery, never localhost. Avoid inventing a
  production URL; validate local rendering before authorized delivery.
- Treat props as untrusted input. Keep JSX interpolation and provider template
  substitution distinct; preserve an explicitly requested placeholder contract.
- Test the changed template's rendered output and relevant client behavior. Report
  client coverage accurately. Rendering a template does not authorize sending it.

## Task references

- [Components](references/COMPONENTS.md): structure and API usage.
- [Styling](references/STYLING.md): email-client CSS and responsive constraints.
- [Patterns](references/PATTERNS.md): examples for the requested email type.
- [Sending](references/SENDING.md): integrating already-rendered templates with a provider.
- [Internationalization](references/I18N.md): localized templates.
- [Editor](references/EDITOR.md): embedding the visual editor only when requested.

Consult [official documentation](https://react.email/docs/llms.txt) for version-sensitive
setup/rendering APIs. Do not scaffold a project or add a visual editor for a template edit.
