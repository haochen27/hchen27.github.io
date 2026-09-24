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

Posts, projects, talks, experience and gallery sections are already written in
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

Every push to `main` builds the site and publishes it with GitHub Pages
(`.github/workflows/deploy.yaml`). Pull requests are built but not deployed, so build errors
show up before merging.

One-time setup: in the repository's **Settings → Pages**, set **Source** to **GitHub Actions**.

The workflow sets the site's base URL from the Pages configuration, so it doesn't need to be
edited if the repository is renamed or a custom domain is added.

## Credits

Based on the [Hugo Academic template](https://github.com/wowchemy/starter-hugo-academic)
by George Cushen (MIT license, see `LICENSE.md`).
