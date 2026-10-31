# yugo

your go to basic hugo theme. black background, white text, cyan links, one column.

[live demo](https://yugo-theme.vercel.app/) · [the kitchen sink](https://yugo-theme.vercel.app/posts/kitchen-sink/), which has one of every element the theme styles

![the example site's home page](https://raw.githubusercontent.com/byanthny/yugo/main/images/screenshot.png)

- one column, black background, white text, cyan links
- plain css. no javascript, no build step, standard hugo is enough
- open graph and twitter cards, rss, syntax highlighting, reading time
- wcag aa contrast throughout
- optional sticky nav, favicon, theme color, footer credit

## install

needs hugo 0.158.0 or newer. the standard build works, extended isn't needed.

as a git submodule:

```sh
git submodule add https://github.com/byanthny/yugo themes/yugo
```

then in `hugo.toml`:

```toml
theme = "yugo"
```

or as a hugo module (needs go installed):

```sh
hugo mod init github.com/you/your-site
```

then in `hugo.toml`:

```toml
[module]
  [[module.imports]]
    path = "github.com/byanthny/yugo"
```

## config

```toml
[params]
  description = "the default meta description"
  stickyNav = true
  favicon = "/favicon.svg"
  appleTouchIcon = "/apple-touch-icon.png"
  themeColor = "#000000"
  images = ["/og.png"]
  themeCredit = true

[menus]
  [[menus.main]]
    name = "posts"
    pageRef = "/posts"
    weight = 10
  [[menus.main]]
    name = "about"
    pageRef = "/about"
    weight = 20

[outputs]
  home = ["html", "rss"]

[markup.highlight]
  style = "github-dark"
```

- `params.description`: used for `<meta name="description">` when a page has no `description` of its own
- `params.stickyNav`: keeps the nav on screen while you scroll. off unless set
- `params.favicon` / `params.appleTouchIcon`: paths to your own icons in `static/`. no tag is written if unset, so nothing 404s
- `params.themeColor`: the browser chrome color on mobile. `#000000` unless set
- `params.images`: the social card image, used when a page sets none of its own. a page can override it with `images` in its front matter
- `params.themeCredit`: adds "built with hugo and yugo" to the footer. off unless set, so your footer stays yours
- `menus.main`: links in the nav, after the site title. with no menu, the nav is just the title
- `outputs`: the home page as html plus the rss feed at `/index.xml`
- `markup.highlight`: the code block colors. any chroma style works, dark ones fit

open graph and twitter card tags are written from each page's title and description, so links shared to chat apps and social sites show something.

## content

- `content/_index.md`: the home page text. under it, the home page lists each section and its pages
- `content/posts/` (or any folder): a section. it gets a list page with each post's date and reading time
- `content/about.md`: a page outside any section. link it from the menu

## run the example

from the theme folder (it has to be named `yugo`):

```sh
hugo server -s exampleSite --themesDir ../..
```

## contributing

contributions are welcome. i'm not actively developing this one, so replies may be slow, but issues
and prs do get read and merged.

likely yes:

- bug fixes
- accessibility fixes
- keeping up with hugo releases
- documentation that makes the theme easier to pick up

likely no:

- javascript
- a build step or css framework
- new layouts or features that make it less minimal

if you're unsure whether something fits, open an issue first and ask rather than building it.

changes are in [CHANGELOG.md](CHANGELOG.md).

## references

- [hugo documentation](https://gohugo.io/documentation/)
- [luke's hugo theme](https://github.com/LukeSmithxyz/lugo)
- [hugo no-style-please theme](https://github.com/Masellum/hugo-theme-nostyleplease)

## license

mit. see [LICENSE](LICENSE).
