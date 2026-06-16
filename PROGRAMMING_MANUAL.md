# Anymatix collection guide

This guide explains how to build a workflow collection others can follow in Anymatix. You do not need to be a programmer — think of it as arranging cards and settings in the app, then exporting JSON.

## What goes in a collection

| Location | Purpose |
|----------|---------|
| `anymatix/*.json` | Workflow files Anymatix imports |
| `assets/` | Images and other files referenced by workflows |
| `PROGRAMMING_MANUAL.md` | This guide (shown inside the app) |

Only `anymatix/*.json` is imported. Other files are ignored for execution.

## Example: Stable Diffusion with optional upscale

Open `anymatix/stable-diffusion.json` in the seed repo. It demonstrates:

- **Workflow switching** — a selector chooses between prompt branches
- **Nested steps** — Base Setup and Upscale are grouped sub-workflows
- **Inputs in different areas** — basic prompts, config sliders, advanced nodes
- **Focus toolbar** — top-level inputs appear when you focus the workflow
- **Optional upscale** — a yes/no toggle includes or skips the upscale step
- **Local assets** — `assets/example-style.png` referenced from the workflow

## Rules for safe collections

1. Put every workflow file in `anymatix/` using `.json` extension.
2. Keep asset paths inside this repository (no `../` escapes).
3. Do not add install scripts, hooks, or executable files expecting Anymatix to run them.
4. Test your JSON in Anymatix after following your own fork.

## Publishing

1. Fork `anymatix/byom` on GitHub.
2. Replace or extend the example workflows.
3. Push your changes — followers can tap **Update** in Anymatix to refresh.

## Getting help

Refer to the in-app Programming System guide for linking workflows together. Your collection JSON uses the same format as Anymatix library projects.
