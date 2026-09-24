# Hao Chen — Personal Website

Source for my academic website, built with [Hugo](https://gohugo.io/) and the
[Wowchemy / Hugo Blox](https://github.com/HugoBlox/hugo-blox-builder) Academic template, and deployed to
GitHub Pages by GitHub Actions. It replaces my old Notre Dame WordPress site
(<https://sites.nd.edu/hao-chen/>).

## Where things live

| What | File |
| --- | --- |
| Name, role, bio, interests, education, social links | `content/authors/admin/_index.md` |
| Profile photo | `content/authors/admin/avatar.jpg` |
| Homepage sections (order, which are shown) | `content/_index.md` |
| Navigation bar | `config/_default/menus.yaml` |
| Site title, URL | `config/_default/config.yaml` |
| SEO description, colors, footer, features | `config/_default/params.yaml` |
| Color palette | `data/themes/teal.toml` |
| Favicon | `assets/media/icon.png` |
| Publications | `content/publication/<slug>/index.md` (+ `cite.bib`) |
| CV (PDF) | `static/uploads/resume.pdf` |
| Gallery photos (captions in `content/_index.md` → `gallery_item`) | `assets/media/albums/gallery/` |

## Adding content

Each content type has a template (archetype) that `hugo new` fills in:

```bash
hugo new content --kind publication publication/my-paper   # then add cite.bib next to index.md
hugo new content --kind post        post/my-first-post
hugo new content --kind project     project/my-project
hugo new content --kind event       event/my-talk
```

In a publication's front matter, list yourself as `admin` in `authors` so your name is
highlighted and linked to your profile. Put a `featured.jpg`/`featured.png` in the page's
folder to give it a thumbnail.

Posts, projects and talks sections are already written in
`content/_index.md` but commented out. Uncomment a section once you have content for it,
and uncomment its link in `config/_default/menus.yaml`.

**CV:** copy your PDF to `static/uploads/resume.pdf`, then uncomment the `CV` entries in
`config/_default/menus.yaml` and `content/authors/admin/_index.md`.

## Previewing locally

Install [Hugo **extended** v0.119.0](https://github.com/gohugoio/hugo/releases/tag/v0.119.0)
and [Go](https://go.dev/dl/) (Hugo uses Go to download the theme), then run:

```bash
hugo server
```

and open <http://localhost:1313/>. The page reloads as you edit.

The theme version is pinned in `go.mod`, and it's tested against Hugo 0.119.0, so newer Hugo
releases may fail to build it. Keep the Hugo version in sync with
`.github/workflows/deploy.yaml` if you change it.

## Deployment

The site is served at <https://haochen27.github.io/> by GitHub Pages, built by
`.github/workflows/deploy.yaml`.

**Publishing is manual for now.** Pushes to `main` and pull requests only build the site
(to catch errors). To publish, open **Actions → Build and deploy site → Run workflow** on
`main`. To publish automatically on every push to `main` instead, follow the comment in
the workflow's "Decide whether to publish" step.

One-time setup:

1. The repository must be named `haochen27.github.io` for the site to be served at the root
   of `https://haochen27.github.io/` (**Settings → General → Repository name**).
2. In **Settings → Pages**, set **Source** to **GitHub Actions**.

The workflow takes the site's URL from the Pages configuration, so nothing else needs to
change if a custom domain is added later.

## Credits

Based on the [Hugo Academic template](https://github.com/wowchemy/starter-hugo-academic)
by George Cushen (MIT license, see `LICENSE.md`).
