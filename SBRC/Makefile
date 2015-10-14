#
# SBRC WPEIF paper Makefile 
#

TEX := pdflatex
BIB := bibtex

SRC := main

BIN := SBRC-2014-WPEIF.pdf

all: wpeif

wpeif: $(SRC).tex
	$(TEX) $^
	$(BIB) $(SRC).aux
	$(TEX) $^
	$(TEX) $^
	@mv $(SRC).pdf $(BIN)
		@echo -e "\n# Type 'make read' to read the output file $(BIN)"

read: $(BIN)
	evince $^

latex: wpeif read

clean:
	@rm -vf *.aux *.pdf *.dvi *.log *.bbl *.blg
