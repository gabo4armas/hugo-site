# Gabriel Cloud Infrastructure and Adoption Hub (Hugo)

A small static website built with [Hugo](https://gohugo.io/) for  the SAP
assignment. It has a home page, an About page, 2 short posts, navigation
between pages and a customized site title. It uses a simple custom layout.

## Prerequisites

* [Hugo](https://gohugo.io/installation/) v0.120 or newer (the standard or the
extended edition both work).
* [Git](https://git-scm.com/) to clone the repository.

### Installing Hugo

|OS|Command|
|-|-|
|macOS|`brew install hugo`|
|Windows|`winget install Hugo.Hugo.Extended`|
|Linux|`sudo snap install hugo` (or download a release from GitHub)|

Check the installation with `hugo version`.

## Run the website locally

```bash
git clone https://github.com/gabo4armas/hugo-site.git
cd hugo-site
hugo server
```

Then open http://localhost:1313/ in your browser to check out the page. Press `Ctrl+C` to stop.

To generate the static files (output goes to `public/`):

```bash
hugo
```

## Project structure

```
hugo.toml            # site title, menu, parameters
content/             # Markdown pages: home, about, posts/
layouts/             # HTML templates (baseof, single, list, home, partials)
static/css/style.css # styling
archetypes/          # template for new content
```

To add a post: `hugo new content posts/my-post.md`

