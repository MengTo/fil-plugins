---
name: "fil-canvas"
description: "Work on a Fil canvas the way Fil expects. Build a flow of prompts, files and generation nodes, price paid runs before they run, wait for results, and keep the canvas tidy. Use for anything made in Fil: pictures, video, 3D, websites, slides, documents, posts and sound."
---

# Working on a Fil canvas

**Start from what's there.** On an existing canvas, call `get_canvas` first: people change canvases between your turns.

**Build the flow, then run it.**
- Put the words in a prompt node (`add_prompt`) and files in file nodes (`add_file`, or `upload_file` first for a file from the person's computer).
- Add the generation node (`add_node`, or `generate` with `kind` and `prompt`) and wire inputs with `connect`.
- One result feeds the next: a picture into a video, a page into a video edit.

**Price, then run.**
- Call `generate` or `edit_image` with `max_credits: 0` to get the price without running. Tell the person the price.
- Run only once they agree: call it again with that `node_id` and `max_credits` set to the price. If they gave you a budget, stay inside it.
- Never raise `max_credits` above what they approved.

**Wait for results.** Runs take seconds to minutes. Call `check_node` with `wait` to get the result, previews and what the run actually cost. Runs hold their maximum and return the rest when they settle.

**Free changes.** Light, colour, grain, blur and vignette go on a picture with `apply_effects`. Files change with `write_file`. A site changes with `set_data`, `set_variables` and `set_component`. Video edits change with `edit_video`. None of these spend credits.

**Keep it in order.** On a large board, `arrange` groups what you made into titled sections in one call. `log` notes a decision or what's next on the canvas's log.

**Privacy.** Work is public or private, node by node. Make something public only when the person asks.

**Publishing.** `publish_site` puts a site on the open web. Do it only when the person asks.
