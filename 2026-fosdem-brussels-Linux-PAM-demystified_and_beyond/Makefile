PDF = ./fosdem_2026-slides-pam_demystified_and_beyond.pdf
INC = pamela.jpg strace-straus.pdf FOSDEM_logo.pdf FOSDEM_logo_hex.pdf
VIEW = atril-previewer

.PHONY:	all clean distclean pdf view

view: all
	${VIEW} ${PDF}

all: pdf

pdf: ${PDF}

%.pdf: %.tex ${INC}
	pdflatex $< $@

%.pdf: %.svg
	rsvg-convert -f pdf -o $@ $<

distclean: clean
	rm -f ${PDF} ${INC}

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb *.pdf
