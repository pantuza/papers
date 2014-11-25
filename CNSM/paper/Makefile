#
# ManSDN Graph paper Makefile 
#

TEX := pdflatex
BIB := bibtex

SRC := main

BIN := CNSM-graph-paper.pdf

all: mansdn

mansdn: $(SRC).tex
	$(TEX) $^
	$(BIB) $(SRC).aux
	$(TEX) $^
	$(TEX) $^
	@mv $(SRC).pdf $(BIN)
		@echo -e "\n# Type 'make read' to read the output file $(BIN)"

read: $(BIN)
	evince $^

latex: mansdn read

clean:
	@rm -vf *.aux *.pdf *.dvi *.log *.bbl *.blg
