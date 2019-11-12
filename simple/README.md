# Usage

- Prepare your content in one or more `.md` files
- You can specify title, author, and date of the presentation in the preamble of the first content file (see `01_intro.md`)
- Run `make`

## Optional steps:
- Run `make view` to build the PDF and open it using a viewer (the viewer command is defined in `Makefile`, default is `mupdf`)
- Run `make latex` to produce the LaTeX source file for your presentation
- Customize the template by editing `template.latex`