---
name: "social-post"
description: "Write a social post in Fil that shows exactly as it will on X, Threads, LinkedIn, Instagram, TikTok or YouTube, with its pictures, video, thread and link card. Use when someone wants a post, a thread, a caption or a YouTube description."
---

# A social post in Fil

1. **Platform and voice.** Ask which platform, unless they said, and what the post is about. Use their own words and facts.
2. **Write it.** Make a Code node with format `post`. Either `generate` it from a prompt naming the platform (priced first), or write it yourself with `write_file`, which is free. The file is the post JSON the server's instructions describe: `platform`, `posts` with each one's `text` and `media`, and a `link` card or `quote` when needed.
3. **Mind the limits.** X counts 280 characters a post (a link is 23), Threads 500, LinkedIn 3,000, Instagram 2,200, TikTok 4,000, a YouTube description 5,000. More than one item is a thread on X and Threads.
4. **Pictures and video.** Make them as nodes (priced first) and point the post's `media` at them as `facet:asset/<id>`.
5. **Suggest, don't overwrite.** To offer a change to words they wrote, add it to that item's `suggestions` with a note. They accept or dismiss it in Fil.
