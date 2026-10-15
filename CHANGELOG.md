# changelog

## v1.0.0 (2026-10-14)

- builds on current hugo again. the sass and `resources.ToCSS` (removed in hugo 0.128) are replaced by one plain css file, minified and fingerprinted, so any hugo build works
- new look: black background, white text, cyan links, system font, one narrow column that fits phones
- templates: head, nav, and footer partials. `lang`, description, canonical, and rss link tags. the home page lists each section's pages, list and single pages show the date and reading time, posts get a back link
- rss works again: removed the empty `rss.xml` that replaced hugo's feed
- inline code stays inline, code blocks scroll inside themselves, no inline styles in the templates
- added theme.toml, LICENSE (mit), an example site, screenshots, and a ci build
- removed the leftover site `config.toml`

## v0.1.0 (2023-03-26)

- first version: base templates, sass, basic content styling
