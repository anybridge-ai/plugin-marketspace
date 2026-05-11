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

A plugin extends Anybridge CLI with new tools, slash commands, themes, hooks, or MCP servers. See the [Anybridge plugin authoring docs](https://github.com/anybridge-ai/coding-agent/blob/dev/docs/plugins/authoring.md).
