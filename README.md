# DocuPress CMS

DocuPress CMS is a Git-backed documentation publishing baseline built with VuePress and Netlify CMS. It combines a static documentation site with a browser-based editorial interface, allowing approved editors to create and review Markdown content through Git Gateway.

## Current capabilities

- VuePress static-site development and production builds
- Netlify CMS administration route at `/admin/`
- Git Gateway backend configuration
- Editorial workflow for draft, review, and publish stages
- Markdown content with title, publication date, and body fields
- Configurable media storage
- Netlify deployment configuration

## Technology stack

| Area | Technology |
| --- | --- |
| Static site generator | VuePress 1.9 |
| Content format | Markdown with front matter |
| Content management | Netlify CMS |
| Authentication | Netlify Identity |
| Git integration | Netlify Git Gateway |
| Hosting | Netlify |

## Prerequisites

- Node.js 14 or newer for the current dependency baseline
- pnpm or npm
- A Netlify account for the hosted CMS workflow

## Local setup

```bash
git clone <repository-url>
cd <repository-directory>
pnpm install
pnpm dev
```

Use the local VuePress URL printed in the terminal. The CMS authentication flow requires a configured Netlify site; local content can still be edited directly as Markdown.

## Commands

| Command | Purpose |
| --- | --- |
| `pnpm dev` | Start the VuePress development server |
| `pnpm build` | Generate the production static site |

## CMS configuration

The CMS definition is stored at `.vuepress/public/admin/config.yml`. The current baseline uses Git Gateway, targets a content branch, stores uploads under `media`, enables editorial workflow, and defines a Markdown post collection. Review the configured branch before enabling the production CMS.

## Configure Netlify

1. Import the repository into Netlify.
2. Enable Netlify Identity.
3. Choose invite-only registration for controlled editorial access.
4. Enable Git Gateway under Identity services.
5. Invite the initial editor account.
6. Confirm the configured CMS branch matches the repository default branch.
7. Visit `/admin/` on the deployed site and complete the sign-in flow.

## Project structure

```text
.vuepress/public/admin/    CMS configuration and admin entry point
README.md                   Project and operator documentation
netlify.toml                Hosting and build configuration
package.json                Scripts and dependency baseline
pnpm-lock.yaml              Reproducible pnpm dependency lock
```

## Security notes

Use invite-only registration for non-public editorial teams, remove former editors promptly, review Git Gateway permissions, and never store service tokens in Markdown or repository files. Treat every CMS-generated change as a normal pull request or editorial review item.

## Roadmap

Planned improvements include a complete VuePress content hierarchy, navigation and sidebar configuration, searchable documentation, accessible layouts, content validation, media rules, preview templates, CMS collections, role guidance, automated link checks, build tests, security headers, dependency modernization, and continuous deployment checks.

## Contributing

Create focused branches from `main`, run `pnpm build`, validate CMS YAML after configuration changes, and describe any migration or operator action required by the pull request.

## License and attribution

This project is distributed under the [MIT License](LICENSE). Existing third-party notices and contributor attribution must remain intact.