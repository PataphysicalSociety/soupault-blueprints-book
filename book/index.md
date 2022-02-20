# Sample book

This is a sample book.

## Adding chapters

You can add more chapters by adding Markdown or HTML files to the `book/` directory.
For example, add `book/02_second_chapter.md`.

Chapter numbers are taken from file names and removed from the output path,
so `book/02_second_chapter.md` becomes `build/second_chapter/index.html`
and can be accessed as `/second_chapter/` when you deploy the book to a web server.

The first `<h1>` of a chapter automatically becomes its title.

## Rendering the book

* Install [soupault](https://soupault.app) 4.0.0 later. 
* Install [pandoc](https://pandoc.org) for Markdown to HTML conversion.
* Run `soupault` in this directory.

The output will be in `build/`.

You can preview it with any web server, e.g. `python3 -m http.server --directory build/`.

## Deploying the book

You can simply upload the contents of the `build/` directory to any web server.

This repository also includes CI scripts for Netlify and Github actions.

The `netlify.sh` script will perform all build and deployment steps for you.

The `.github/workflows/main.yaml` also includes steps for deploying to Netlify, but you can easily replace
those with your own deployment steps.

## Styling the book

The CSS file is in `book/styles/main.css`. Most things can be changed with CSS variables there.

## Configuring soupault

The configuration file is `soupault.toml`.

Some things you may want to change:

* The `<title>` settings in `[widgets.page-title]`
* The sidebar template in `[insert-chapters-index]`
