# Usage

- Prepare your content in one or more `.md` or `.tex` files
- Add an `\input{filename_without_extension}` line in `content.tex` for each source file you have
- Run `make`

# Switching to LaTeX-only development
Every time you run `make`, each `.md` source file is converted to a `.tex` fie using pandoc. If at some point you want to directly work on the LaTeX source code, you can run:

```
make archive_markdown
```

The command above creates an archive with all the markdown source files and removes them from the working directory. You can still build the slides running `make`.

In case you want to restore the Markdown source files:

```
make restore_markdown
```