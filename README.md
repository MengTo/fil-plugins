# Fil plugins

[Fil](https://fil.design) is a canvas for making images, video, 3D, websites, slides and social posts with the best models. This plugin brings it to Claude Code: Fil's MCP server, so Claude works on your canvas live, and Fil's skills.

## Claude Code

In Claude Code (the terminal, or the Code tab of the Claude desktop app):

```text
/plugin marketplace add https://github.com/MengTo/fil-plugins
/plugin install fil@fil
```

Then run `/mcp`, pick fil and sign in: Fil opens in your browser to allow it, with a daily cap on the credits it can spend. In the desktop app, once the marketplace is added, the plugin is also under **+** › **Add plugins**.

From a shell:

```bash
claude plugin marketplace add https://github.com/MengTo/fil-plugins
claude plugin install fil@fil
```

## What's in it

- **Fil's MCP server** (`https://fil.design/mcp`): canvases, prompts, files and generation nodes, sites, video edits. Runs that spend credits are priced first.
- **Skills**: `/fil:setup` to get started, `fil-canvas` for working on a canvas, `landing-page`, `story-video`, `social-post`, and Fil's [HTML Demo](https://fil.design/skills/html-demo), [HTML Reel](https://fil.design/skills/html-reel) and [HTML Explainer Video](https://fil.design/skills/html-explainer-video).

## ChatGPT

Fil also works in ChatGPT: see [Use Fil in ChatGPT](https://fil.design/docs/chatgpt).

Fil is invite-only for now; the plugin works once you have a Fil account.
