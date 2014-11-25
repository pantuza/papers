#
# CNSM graph paper Makefile
#


TEX := pdflatex
BIB := bibtex


SRC := main

BIN := CNSM-graph-presentation.pdf

all: graph

graph: $(SRC).tex
	$(TEX) $^
	$(TEX) $^
	@mv $(SRC).pdf $(BIN)
	@echo -e "\n# Type make read to read the output file $(BIN)"

latex: graph read

read: $(BIN)
	evince $^

clean:
	@rm -vf *.aux *.pdf *.dvi *.log *.bbl *.blg \
		*.bak *.nav *.out *.snm *.toc *.vrb
