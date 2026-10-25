---
name: "landing-page"
description: "Make a landing page or website in Fil from a brief. A Code node writes the site, then you refine its pages, design system and content, and publish it when asked. Use when someone wants a landing page, a homepage, a product page or a small site."
---

# A landing page in Fil

1. **Brief.** Get what it's for, who it's for, the sections it needs, and the look: words, a reference site or a picture. Put the brief in a prompt node. Add references as files.
2. **Write it.** Add a Code node with format `site` (the default), wired to the prompt and references. Price it with `generate` and `max_credits: 0`, show the price, and run once approved. Wait with `check_node`.
3. **Read what was made.** `get_site` shows its pages, its design system (colours, fonts, text styles, components) and its data. `read_file` reads any of them.
4. **Refine for free.**
   - `set_data` changes the words and lists.
   - `set_variables` changes colours, fonts and text styles.
   - `set_component` changes a component on every page that uses it.
   - `write_file` rewrites a page.
   - `add_page` adds a page linked into the navigation.
5. **Pictures.** Make them as image nodes (priced first), then put them on the page through its data or files.
6. **Publish only when asked.** `set_site` sets its name, SEO, address and password. `publish_site` puts it live and gives its address.
