# Screen Reader Testing

## Purpose

Define the screen reader testing standard for DocuPress CMS so VuePress content and Netlify CMS editorial changes remain secure, reviewable, and deployable.

## Current baseline

DocuPress CMS uses VuePress 1.9, Markdown, Netlify CMS, Netlify Identity, Git Gateway, and an editorial workflow. This guide separates current behavior from planned improvements.

## Acceptance criteria

- The screen reader testing requirement is explicit and testable.
- Editor, reviewer, and reader impact is considered.
- CMS branch and Git Gateway behavior are documented.
- Security, accessibility, and content-migration impact is covered.
- Recovery or rollback steps are clear.

## Verification checklist

- [ ] Run `pnpm build`.
- [ ] Validate affected YAML or front matter.
- [ ] Check the generated documentation route.
- [ ] Exercise `/admin/` when CMS behavior changes.
- [ ] Confirm no service tokens or private content are committed.

## Review guidance

Keep implementation work focused on one screen reader testing outcome and note any Netlify operator action in the pull request.