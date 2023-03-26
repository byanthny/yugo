# Yugo - your go to hugo theme

simple hugo theme for my projects and skeleton for future themes

## setup

see [hugo docs](https://gohugo.io/categories/getting-started/) for more updated and thorough instructions

```sh
hugo new site <sitename>
cd <sitename>
git init
git submodule add https://github.com/byanthny/yugo
echo 'theme = "yugo"' >> config.toml
hugo server
```

put homepage content in root layout/index.html
not the theme folder

# Roadmap

See `CHANGELONG.md` for changes.

- [x] main page templates
- [x] initial sass files
- [x] basic content styling
- [ ] back links
- [ ] more components (posts list, image gallery, latex)
- [ ] more content styling
- [ ] rss

---

## references and learning resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Luke's Hugo Theme](https://github.com/LukeSmithxyz/lugo)
- [Hugo no-style-please Theme](https://github.com/Masellum/hugo-theme-nostyleplease)
