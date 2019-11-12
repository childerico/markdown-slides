MD_SOURCES = $(wildcard *.md)
TEMPLATE = template.latex
PDF = slides.pdf
TEX_OUTPUT = $(PDF:.pdf=.tex)
VIEWER = mupdf

all: $(PDF)

$(PDF): $(MD_SOURCES) $(TEMPLATE)
	pandoc --template $(TEMPLATE) -t beamer $(MD_SOURCES) -o $@

latex: $(TEX_OUTPUT)

$(TEX_OUTPUT): $(MD_SOURCES) $(TEMPLATE)
	pandoc --template $(TEMPLATE) -t beamer $(MD_SOURCES) -o $@

view: $(PDF)
	$(VIEWER) $(PDF)

clean:
	-rm $(PDF) $(TEX_OUTPUT)

.PHONY: clean





