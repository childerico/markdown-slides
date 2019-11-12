# markdown-slides
I like to use Markdown to prepare (at least) the initial draft of my presentations.
This repository shows how to build a Beamer (LaTeX) presentation starting with a bunch of Markdown files. We rely on **pandoc** and **make**.

Two examples are available, in two different directories:

- `simple`: just create some `.md` files and run `make`
- `full`: requires a bit of configuration, but allows to mix LaTeX and Markdown source files, and to switch completely to LaTeX-based development after the initial phase of drafting

## Requirements
For `simple` and `full` :

- make
- pandoc
- LaTeX

For `full` only:

- tar
- latexmk

## Usage
See `README.md` in the subdirectories.
