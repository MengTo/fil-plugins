---
name: "story-video"
description: "Make a short story video in Fil. Write the shots, make a picture for each, bring them to life as videos, add a voice or music, and cut it all together in Fil's video editor. Use when someone wants a short film, an ad, a trailer or a story told in shots."
---

# A story video in Fil

1. **Script the shots.** Write the story as 4 to 8 shots, one line each: what's seen, the camera, the mood. Put each in its own prompt node, in order.
2. **Keep one look.** Make the main character or product as one picture first and wire it into every shot's image node, so they all match.
3. **Pictures, then video.** Add an image node per shot and price the whole set (`generate` with `max_credits: 0`, node by node). Give the total, and run once approved. Then wire each picture into a video node for its motion, priced and approved the same way.
4. **Sound.** Add a voiceover or music node if the story needs one, priced like the rest.
5. **Cut it.** `make_video` takes the shot videos in order, with the sound under them, as one Video edit node. `edit_video` trims, reorders and adds transitions, titles and captions. Everything but captions is free; captions cost a few credits by length.
6. **Export.** `export_video` makes the MP4 in the person's open Fil studio. `check_node` with `wait` gives its link when it's done.
