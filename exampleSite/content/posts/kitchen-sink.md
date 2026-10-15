---
title: "kitchen sink"
date: 2026-10-14
description: "every element the theme styles, on one page"
draft: false
---

one of each element the theme styles. check this page after a change. links look [like this](https://gohugo.io/documentation/).

## headings

the title is an `h1`, and this section starts with an `h2`.

### a third-level heading

#### a fourth-level heading

## lists

- a list item
- a list item with `inline code`
  - a nested item
  - another nested item
    - one more level
- back to the top level

1. first
2. second
3. third

## code

inline code like `hugo server` stays in the line. a fenced block gets its own box:

```go
package main

import "fmt"

func main() {
	words := []string{"black", "white", "cyan"}
	for i, w := range words {
		fmt.Printf("%d: %s\n", i, w)
	}
	fmt.Println("this line is long on purpose, so the block scrolls sideways on a narrow screen and the page does not")
}
```

## quote

> a blockquote gets a thin line on the left and muted text.

## table

| part | color |
| --- | --- |
| background | `--ink` |
| text | `--body` |
| headings | `--fg` |
| links | `--accent` |

## image

![a sample image: gray bars and a cyan ring on a dark background](/img/sample.svg)

---

the line above is a horizontal rule.
