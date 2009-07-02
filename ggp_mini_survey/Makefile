# Makefile for sbgames latex template
#

LATEX=pdflatex
BIBTEX=bibtex
MAIN_PDF=artigo.pdf
MAIN_TEX=main
MAIN_BIB=main

all: artigo 

artigo: src/${MAIN_TEX}.tex src/${MAIN_BIB}.bib
	cd src/						&& \
	$(LATEX)  ${MAIN_TEX}.tex 	&& \
	$(BIBTEX) ${MAIN_BIB}		&& \
	$(LATEX)  ${MAIN_TEX}.tex	&& \
	$(LATEX)  ${MAIN_TEX}.tex
	@mv src/${MAIN_TEX}.pdf ./$(MAIN_PDF)	


clean:
	@rm -f src/*{.aux,.log,.toc,.nav,.out,.snm,.vrb,.bbl,.blg}
