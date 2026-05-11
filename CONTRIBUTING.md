# Contributing a plugin

Welcome — this guide is for plugin authors who want their plugin listed in the official Anybridge marketplace.

## Steps

1. **Write your plugin** against the `@anybridge-ai/plugin` SDK. See [authoring docs](https://github.com/anybridge-ai/coding-agent/blob/dev/docs/plugins/authoring.md).
2. **Publish your plugin** to **npm** (recommended) or **GitHub** (any public repo with a valid `package.json` at root).
3. **Fork this repo**, edit `marketplace.json`, add an entry to the `plugins` array:

   ```json
   {
     "name": "your-plugin-name",
     "source": "npm:your-package-name",
     "version": "1.0.0",
     "description": "Brief one-line description",
     "author": "Your Name",
     "license": "MIT",
     "homepage": "https://github.com/you/your-plugin",
     "keywords": ["category", "tag"],
     "category": "Productivity"
   }
   ```

   For GitHub-sourced plugins, use `"source": "github:owner/repo"` instead.

4. **Open a Pull Request**. A maintainer will review using the checklist below.

## PR review checklist

- [ ] `name` doesn't collide with an existing plugin
- [ ] `source` URL resolves (npm package exists / GitHub repo exists)
- [ ] `description` accurately reflects what the plugin does
- [ ] `license` declared (SPDX identifier)
- [ ] Quick code skim — no `eval()`, no arbitrary external URL fetches, no environment-variable dumps, no autonomous external-app launches
- [ ] README at the source repo explains usage
- [ ] Plugin works with the current Anybridge SDK version (`engines.anybridge`)

## What gets rejected

- Plugins with no source / dead links
- Plugins duplicating existing functionality with no clear improvement
- Plugins shipping non-MIT/Apache licenses without justification
- Plugins that contain ads, telemetry, or autonomously open external apps
- Plugins that bundle secrets or hardcoded credentials

## Categories

When you set `category` in your entry, pick the closest fit from:

- `Productivity` (Jira, Linear, Notion, etc.)
- `Theme` (color themes)
- `Utility` (formatters, linters, search tools)
- `Integration` (Slack, Discord, email)
- `Development` (git, deployment, build helpers)
- `Other`

## Version bumps

To roll out an updated version, bump the `version` field in your `marketplace.json` entry to match your latest published version. Users running `anybridge plugin upgrade` will pick it up on the next 24-hour check cycle.
