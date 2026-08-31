# Privacy Model

## Purpose

Define how DocuPress CMS handles editor identity, repository content, uploaded media, and deployment metadata.

## Acceptance criteria

- Data collection and retention are explicit.
- Netlify Identity and Git Gateway responsibilities are separated.
- Private content and tokens are never committed.
- Removal and recovery behavior is documented.

## Verification

- [ ] Run `pnpm build`.
- [ ] Inspect CMS configuration.
- [ ] Confirm no private values are committed.