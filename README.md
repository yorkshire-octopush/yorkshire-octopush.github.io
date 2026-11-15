# Yorkshire Octopush Juniors website

A one-page website for Yorkshire Octopush Juniors, built with Jekyll so that GitHub Pages turns the Markdown files into the finished site automatically. There is nothing to install and no build step.

## Where the site lives

The site is published at https://yorkshire-octopush.github.io/ from the repository `yorkshire-octopush/yorkshire-octopush.github.io`, which belongs to the GitHub organisation `yorkshire-octopush`. GitHub Pages rebuilds the site automatically a minute or two after each change is pushed to the `main` branch. Other club members can be given access by adding them to the organisation.

If you later give the site its own domain, change `url` in `_config.yml` and add the domain under Settings → Pages.

## Editing the content

| What you want to change | Where |
|---|---|
| Email address, training day, time and venue, logo, banner image | `_config.yml` |
| The text of each part of the page | `_sections/*.md` (one file per section) |
| Colours and fonts | top of `assets/css/style.css` |
| Photos | drop `.jpg` or `.png` files into `assets/img/gallery/` |

Each file in `_sections` is ordinary Markdown with a short header between `---` lines giving its title, its label in the menu and its background colour (`light`, `tint` or `dark`). The sections appear in file-name order, so to add a new section create e.g. `_sections/045-competitions.md`, and to remove one delete the file. HTML can be used inside the Markdown wherever you need it.

Text that still needs writing is marked `TODO` and appears on the page in yellow boxes. Search the folder for `TODO` to find them all, and delete each `<span class="todo">…</span>` once you have replaced it.

## Images

- `assets/img/logo.svg` is a placeholder. Replace it with the club logo (any name, e.g. `logo.png`) and update `logo:` in `_config.yml`. Do the same for `favicon.svg`, the small icon in the browser tab.
- `assets/img/hero.svg` is an illustration used as the banner. To use a photo instead, add it (ideally at least 1600 pixels wide, landscape) and change `hero_image:` in `_config.yml`.
- Make sure you have permission to publish any photos of children, and that parents have consented.

## Previewing on your own computer (optional)

You don't need this, since GitHub builds the site for you, but if you want to preview changes before pushing:

```
gem install jekyll webrick kramdown-parser-gfm
jekyll serve
```

then open http://localhost:4000/
