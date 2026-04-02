# phqmd.github.io

Website for the **Parton-Hadron-String Dynamics (PHSD)** transport code, built with [Hugo](https://gohugo.io/) and the [Beautiful Hugo](https://themes.gohugo.io/themes/beautifulhugo/) theme.

Live site: [phqmd.github.io](https://phqmd.github.io)

---

## Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version recommended)

---

## Local development

1. Clone the repository:
   ```bash
   git clone https://github.com/phqmd/phqmd.github.io.git
   cd phqmd.github.io
   ```

2. Start the local development server:
   ```bash
   hugo server
   ```
   The site will be available at `http://localhost:1313/`.

3. To include draft pages:
   ```bash
   hugo server -D
   ```

---

## Adding or editing content

All pages live in the [content/](content/) directory as Markdown files:

| File | Page |
|------|------|
| `content/_index.md` | Home page |
| `content/about.md` | About PHSD |
| `content/code.md` | Code |
| `content/publications.md` | Publications |
| `content/talks.md` | Talks |
| `content/team.md` | Team |

Edit the relevant `.md` file and the change will be reflected immediately when `hugo server` is running.

### Front matter

Each page starts with a TOML/YAML front matter block, for example:

```markdown
---
title: "About PHSD"
draft: false
---
```

Set `draft: true` to hide a page from the published site (it will still appear with `hugo server -D`).

### Images and static files

Place images and other static assets in [static/img/](static/img/). Reference them in Markdown as:

```markdown
![Alt text](img/filename.png)
```

---

## Site configuration

Global settings (title, theme, navigation menu, etc.) are in [config.toml](config.toml).

To add a new menu entry, append a block like this:

```toml
[[menu.main]]
  name = "New Page"
  url  = "new-page"
  weight = 6
```

Then create the corresponding `content/new-page.md`.

---

## Building for production

```bash
hugo
```

The generated site is written to the `public/` directory. This directory is deployed automatically via GitHub Actions on every push to `main`.

---

## License

See [LICENSE](LICENSE).
