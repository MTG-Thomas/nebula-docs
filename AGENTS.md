# Nebula documentation

Docusaurus/TypeScript documentation for the Nebula networking project. `docs/` holds documentation, `src/` site customizations, `static/` assets, and `sidebars.js` plus `docusaurus.config.ts` control navigation/site behavior. Read [README.md](README.md) and the page being changed before editing commands, certificate examples, or network configuration.

## Development and checks

Use the package manager recorded in `package.json`: `pnpm@9.7.0`. Node must satisfy `engines` (`>=18`); consult `.nvmrc` for the project-selected version. From root run `pnpm install`, `pnpm format:check`, `pnpm typecheck`, `pnpm test`, and `pnpm build`. `pnpm start` previews locally; `pnpm preview` serves the built output.

The build and postinstall scripts invoke `parse-domain-update`, so those commands can refresh supporting domain data. Review resulting changes; keep dependency/generated-data changes separate from prose-only corrections. Prefer `format:check` for validation because `pnpm format` rewrites the entire tree.

## Documentation rules

Preserve working MDX imports, frontmatter, links, and navigation; use neighboring pages' patterns. Validate changed pages in the local site, including mobile navigation and code blocks when relevant. Documentation examples must accurately distinguish certificate identity, trusted CA material, firewall policy, and deployment steps; never insert real private keys or credentials into examples.

Keep this working fork usable while preserving upstream conventions. Explain any MTG-specific instructions clearly rather than silently changing general upstream product behavior. Package scripts verify site structure and tests; they do not prove commands against a live Nebula mesh. Site publishing and live VPN operations require their own scoped procedure and readback.
