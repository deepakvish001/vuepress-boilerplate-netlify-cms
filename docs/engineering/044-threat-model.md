# Threat Model

## Purpose

Define the threat model standard for DocuPress CMS so VuePress content and Netlify CMS editorial changes remain secure, reviewable, and deployable.

## Current baseline

DocuPress CMS uses VuePress 1.9, Markdown, Netlify CMS, Netlify Identity, Git Gateway, and an editorial workflow.

## Acceptance criteria

- The threat model requirement is explicit and testable.
- Editor, reviewer, and reader impact is considered.
- CMS branch and Git Gateway behavior are documented.
- Security, accessibility, and migration impact is covered.
- Recovery or rollback steps are clear.

## Verification checklist

- [ ] Run `pnpm build`.
- [ ] Validate affected YAML or front matter.
- [ ] Check the generated documentation route.
- [ ] Exercise `/admin/` when CMS behavior changes.
- [ ] Confirm no tokens or private content are committed.