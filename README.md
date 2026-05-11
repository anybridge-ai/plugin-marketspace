# Anybridge AI Plugin Marketplace

This repo is the **official Anybridge plugin catalog**. The single `marketplace.json` file lists all plugins available to the Anybridge CLI through the `@anybridge` marketplace identifier.

## Use it from your CLI

```bash
anybridge marketplace add anybridge anybridge-ai/plugin-marketspace
anybridge plugin search <query>
anybridge plugin install <name>@anybridge
```

## Submit a plugin

See [CONTRIBUTING.md](./CONTRIBUTING.md).

## What's a plugin?

A plugin extends Anybridge CLI with new tools, slash commands, themes, hooks, or MCP servers. Plugin authors write packages against the `@anybridge-ai/plugin` SDK and submit them here via the steps in [CONTRIBUTING.md](./CONTRIBUTING.md).

For now, plugin authoring guidance ships with the Anybridge CLI itself — run `anybridge plugin --help` or open the `/plugins` browser inside the TUI. A dedicated public authoring guide will land alongside the first beta release.
