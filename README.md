# soupault-blueprints-book

A ready-to-use [soupault](https://soupault.app) setup for creating books,
comparable to [mdBook](https://rust-lang.github.io/mdBook/).

If you want to see a real book based on this blueprint, check out
[OCaml From the Ground Up](https://ocamlbook.org).

## Dependencies

You need soupault 4.0.0 or later to use this blueprint.

The default setup relies on [pandoc](https://pandoc.org) for Markdown to HTML conversion.
See the `[preprocessors]` section in `soupault.toml`.

However, you can configure different pandoc options, replace it with a different Markdown
processor of your choice, or add convertors for different formats (reStructuredText, AsciiDoc...).
See the [page preprocessors section](https://soupault.app/reference-manual/#page-preprocessors)
of the soupault reference manual.

## Adding chapters

The sidebar with a list of chapters is generated completely automatically.
There's no need to write a ToC/summary of the book by hand.

Chapter numbers are taken from file names. In the sample setup,
there are `book/00_preface.md` and `book/01_sample_chapter.md`.

Those numbers are also removed from output file paths,
so you will get clean `/preface/` and `/sample_chapter` URLs instead.

## Configuring the book

The configuration file is `soupault.toml`.

### Book title

You can set the title that appears in the HTML `<title>` by editing the `[widgets.page-title]`
section in the config.

### Modifying the sidebar ToC

The template for rendering the chapters index is in the `widgets.chapters-index.index_template` option.

