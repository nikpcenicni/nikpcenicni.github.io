# nikpcenicni.github.io

My personal site, live at **[pcenicni.dev](https://pcenicni.dev)**.

A small static page: plain HTML, CSS and JavaScript with no build step, served by GitHub Pages.

## What's on it

- **About** — who I am, my homelab, and the tools I use.
- **Projects** — pulled live from my public GitHub repos. You can filter them by name or language, and archived repos are listed separately at the bottom.
- **Contact** — a form that sends messages to my inbox through [FormSubmit](https://formsubmit.co).

## How the projects list works

`main.js` fetches my repos from the GitHub API when the page loads and caches them in the browser for an hour, because the API only allows 60 requests an hour without signing in. The settings at the top of the file control what shows up:

| Setting | What it does |
| --- | --- |
| `HIDDEN` | Repos that never appear on the site. |
| `INCLUDE_FORKS` | Forks are hidden unless they're listed here. |
| `FEATURED` | Custom emoji and descriptions. Repos listed here are shown first, in this order. |
| `PAGES_DOMAIN` | The custom domain used for links to GitHub Pages sites. |

A project's name links to its website when it has one: the website set on the repo, or its GitHub Pages site. The repo itself is linked from the card's "repo ↗" link. Projects without a website link straight to the repo.

## Running it locally

Serve the folder with any static file server, for example:

```sh
python3 -m http.server
```

Then open <http://localhost:8000>.

## Deploying

Pushing to `main` publishes the site. The `CNAME` file points GitHub Pages at `pcenicni.dev`.
