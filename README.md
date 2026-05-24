# Forty (Hugo)

A Hugo port of the [HTML5 UP **Forty**](https://html5up.net/forty) one-page
template by [@ajlkn](https://twitter.com/ajlkn). The original is free for
commercial use under the [CC BY 3.0](LICENSE) license — keep the credit link
in the footer.

This port turns the single hand-edited `index.html` into a small, data-driven
Hugo theme: the banner, the tiles, the about section, and the contact section
all read from `data/sitetext.yml` + `data/navigation.yml`, so you change copy
without touching markup. The CSS ships precompiled (under `static/assets/css`),
so there is **no build step** — the Sass source is kept in `src/sass` for
reference only.

## Use it

```toml
# hugo.toml
theme = "html5up-forty-hugo"
```

or as a Hugo Module / git submodule under `themes/`.

## Customize

| What | Where |
|------|-------|
| Banner / tiles / about / contact copy | `data/sitetext.yml` (keyed by locale) |
| Off-canvas menu links | `data/navigation.yml` |
| Images | `static/images/` (or absolute paths to your own) |
| Colors, fonts | `src/sass/*` then recompile to `static/assets/css/main.css` |

### Injection hooks

Three empty partials let a consuming site add markup without overriding
`baseof.html`:

- `partials/head-top.html` — emitted in `<head>` **before** the stylesheet
  (good for a pre-paint theme/palette script).
- `partials/head-extra.html` — emitted in `<head>` **after** the stylesheet
  (good for style overrides).
- `partials/body-end.html` — emitted at the end of `<body>` (good for a
  floating widget).

## Credit

Design: [HTML5 UP](https://html5up.net) · CC BY 3.0. Hugo port by David Watson.
