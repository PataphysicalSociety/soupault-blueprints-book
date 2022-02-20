# soupault-blueprints-book

A ready-to-use [soupault](https://soupault.app) setup for creating books,
comparable to [mdBook](https://rust-lang.github.io/mdBook/).

## Dependencies

This setup relies on [pandoc](https://pandoc.org) for Markdown to HTML conversion.
See the `[preprocessors]` section in `soupault.toml`.

You can configure different pandoc options, replace it with a different Markdown
processor of your choice, or add convertors for different formats (reStructuredText, AsciiDoc...).
See the [page preprocessors section](https://soupault.app/reference-manual/#page-preprocessors)
of the soupault reference manual.

## Adding chapters

Chapters are numbered automatically in the sidebar.
There's no need to write a ToC/summary of the book by hand.

Chapter numbers are taken from file names. In the sample setup,
there are `book/00_preface.md` and `book/01_sample_chapter.md`.

Those numbers are also removed from output file paths,
so you will get clean `/preface/` and `/sample_chapter` URLs instead.

## Modifying the sidebar ToC



