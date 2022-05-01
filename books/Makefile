ALL=$(shell echo *.tex)

watch:  ## Recompile on any update of LaTeX or SVG sources
	while true; do inotifywait *.tex ; make all; done

all: $(addsuffix .pdf, $(basename $(ALL)))

%.pdf %.aux %.idx: %.tex
	pdflatex \\nonstopmode\\input $<
