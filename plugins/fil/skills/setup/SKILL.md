---
name: "setup"
description: "Set up Fil the first time it's used in a conversation. Signs the person in to Fil, checks their account, and makes or opens a canvas to work on, with its link. Use when Fil was just connected, when the person asks what Fil can do, or before the first thing they ask Fil to make."
---

# Getting started with Fil

1. Call `get_account`. It says who is signed in, their workspaces and their credits. If it can't, the person connects Fil again from the plugin's settings and approves it in the browser.
2. Ask what they want to make, unless they already said. Fil makes images, video, 3D models, websites, slides, documents, social posts and audio, as nodes on a canvas.
3. Find a canvas with `list_canvases`, or make one with `create_canvas` named after what they're making. Give them its link: what you make shows there live, and they can open it in Fil to keep going.
4. Tell them once how paid runs work. `generate` and `edit_image` spend Fil credits. You price a run first (`max_credits: 0`) and show the price, and nothing runs until they approve it, or until they give you a budget to work within. Writing files, editing a site, video edits and effects are free.

Then follow the `fil-canvas` skill for the work itself.
