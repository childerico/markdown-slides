TEX_MAIN = slides.tex
VIEWER = mupdf
# -----------------------------------------
MD_SOURCES = $(filter-out README.md, $(wildcard *.md))
TEX_SOURCES = $(MD_SOURCES:.md=.tex)
PDF = $(TEX_MAIN:.tex=.pdf)
MD_ARCHIVE = markdown.tar.gz

all: $(PDF) 

$(PDF): $(TEX_SOURCES) 
	latexmk -pdf $(TEX_MAIN)

%.tex: %.md
	pandoc -t beamer $^ > $@

view: $(PDF)
	$(VIEWER) $(PDF)

clean:
	-rm $(TEX_SOURCES)
	-latexmk -c $(TEX_MAIN)

archive_markdown:
	tar czf $(MD_ARCHIVE) $(MD_SOURCES)
	rm $(MD_SOURCES)

restore_markdown:
	tar xzf $(MD_ARCHIVE)
	rm $(MD_ARCHIVE)


.PHONY: clean $(PDF) archive_markdown restore_markdown





