# khorum-ai-marketplace

Curated Claude Code plugins and skills from Khorum OSS, organized by functionality.

## Install

Add the marketplace once:

```
/plugin marketplace add khorum-oss/khorum-ai-marketplace
```

Then install any plugin by name:

```
/plugin install <plugin>@khorum-ai-marketplace
```

## Catalog

| Category | Plugin | What it does |
|---|---|---|
| [Media Production](plugins/media-production) | `argo-guide` | Product demo videos from Playwright scripts, with AI voiceover and overlays. |
| [Observability](plugins/observability) | `foreman-vision` | Live pixel-art office view of Claude Code sessions and subagents. |
| [Diagramming](plugins/diagramming) | `daidal-diagram` | Architecture and system diagrams drawn inline in the chat, as Daidal diagrams. |
| [Developer Tools](plugins/developer-tools) | _none yet_ | Code review, testing, scaffolding, release tooling. |

## Layout

```
.claude-plugin/marketplace.json   # the catalog Claude Code reads
plugins/
  <category>/                     # one folder per functional area
    README.md                     # lists every plugin in the category
    <plugin>/                     # plugins hosted in this repo
      .claude-plugin/plugin.json
      skills/ commands/ agents/ hooks/ .mcp.json
templates/plugin-template/        # copy to start a new plugin
scripts/validate.mjs              # layout checks, run in CI
```

A plugin either lives in this repo under `plugins/<category>/<plugin>/`, or stays in its own
repository and gets referenced from `marketplace.json` with a `github` source. Either way its
entry carries a `category` that matches a folder under `plugins/`, and that folder's README lists it.

See [CONTRIBUTING.md](CONTRIBUTING.md) to add a plugin or a category.
