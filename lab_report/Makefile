manuscript = report
latexopt   = -halt-on-error -file-line-error

all: $(manuscript).pdf

$(manuscript).pdf: $(manuscript).tex references.bib
	pdflatex $(latexopt) $<
	bibtex $(basename $<).aux
	pdflatex $(latexopt) $<
	pdflatex $(latexopt) $<
	evince $(manuscript).pdf

clean:
	@rm -f *.aux *.bbl *.blg *.log *.out *.spl *.dvi $(manuscript).pdf

.PHONY: all clean
