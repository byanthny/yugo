# changelog

## v1.0.1 (2026-10-30)

- `hugo.toml` declares the supported hugo versions under `[module.hugoVersion]`, which is what themes.gohugo.io reads. `theme.toml`'s `min_version` is a different field and is not a substitute
- the readme's screenshot uses an absolute url. relative paths work on github but break on the theme's page at themes.gohugo.io

## v1.0.0 (2026-10-14)

- builds on current hugo again. the sass and `resources.ToCSS` (removed in hugo 0.128) are replaced by one plain css file, minified and fingerprinted, so any hugo build works
- new look: black background, white text, cyan links, system font, one narrow column that fits phones
- templates: head, nav, and footer partials. `lang`, description, canonical, and rss link tags. the home page lists each section's pages, list and single pages show the date and reading time, posts get a back link
- rss works again: removed the empty `rss.xml` that replaced hugo's feed
- inline code stays inline, code blocks scroll inside themselves, no inline styles in the templates
- added theme.toml, LICENSE (mit), an example site, screenshots, and a ci build
- removed the leftover site `config.toml`
- `<html lang>` follows the site's configured `locale` instead of always printing the language key, so a non-english site is no longer announced as english
- needs hugo 0.158.0 or newer. that release renamed `languageCode` to `locale` and deprecated the old template accessors
- the example site turns taxonomies off, so it no longer ships empty `/tags/` and `/categories/` pages
- ci builds on the oldest supported hugo as well as the latest
- a vercel demo site builds from `exampleSite/`
- optional sticky nav: set `params.stickyNav` to keep it on screen while scrolling. off unless set
- open graph and twitter card tags, so shared links no longer preview blank
- optional favicon, apple touch icon, and theme color params. nothing is written unless set
- a live demo at https://yugo-theme.vercel.app, linked from the readme and `theme.toml`

## v0.1.0 (2023-03-26)

- first version: base templates, sass, basic content styling
