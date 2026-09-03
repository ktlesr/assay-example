---
name: hello-manifest
description: Turns a list of dashboard tiles into a widget manifest JSON file. Use when the user asks to turn notes or a draft into a widget manifest, or to build a dashboard manifest from a list of tiles.
---

# Hello manifest

Write the manifest to the relative path `out/manifest.json`.

Resolve that path against the **current working directory**, not against this
skill's base directory. Use the file-writing tool directly — it creates parent
directories for you. Do not run shell commands.

The file must be valid JSON with this shape:

```json
{
  "title": "<dashboard title from the request>",
  "widgets": [
    { "id": "<slug>", "type": "tile", "title": "<label>" }
  ]
}
```

After writing the file, say in one sentence what you wrote.
