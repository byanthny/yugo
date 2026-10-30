# yugo

a basic dark hugo theme: black background, white text, cyan links, one column.

[live demo](https://yugo-theme.vercel.app/) · [the kitchen sink](https://yugo-theme.vercel.app/posts/kitchen-sink/), which has one of every element the theme styles

![the example site's home page](https://raw.githubusercontent.com/byanthny/yugo/main/images/screenshot.png)

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

## maintenance

v1 is done. no roadmap. issues and small prs welcome, fixes land when i get to them.

changes are in [CHANGELOG.md](CHANGELOG.md).

## references

- [hugo documentation](https://gohugo.io/documentation/)
- [luke's hugo theme](https://github.com/LukeSmithxyz/lugo)
- [hugo no-style-please theme](https://github.com/Masellum/hugo-theme-nostyleplease)

## license

mit. see [LICENSE](LICENSE).
