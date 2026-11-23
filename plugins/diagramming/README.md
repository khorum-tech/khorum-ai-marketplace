# Diagramming

Plugins that draw or edit diagrams of systems: architecture, data flow, C4 views, deployments.

| Plugin | Hosted | What it does |
|---|---|---|
| [`daidal-diagram`](https://github.com/khorum-tech/daidal/tree/main/skills/daidal-diagram) | external (`khorum-tech/daidal`) | Draws a system inline in the chat as a Daidal diagram, from a config Claude writes or one you paste. The config pastes straight into Daidal. |

```bash
/plugin install daidal-diagram@khorum-ai-marketplace
```

The picture is drawn by Daidal's own renderer, `@khorum/daidal-core`, loaded from an npm CDN at a pinned
version. If the CDN can't serve it, the skill shows the config as text instead.
