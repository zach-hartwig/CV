texlist := $(wildcard *.tex)

TARGET := ZachHartwig_CV_Full.pdf

$(TARGET): cv_full.ps
	ps2pdf $< $@
	@rm *.dvi *.ps *.log *.toc *.aux *.out *.idx *.ilg *.ind *.spl *.bbl *.blg -f >& /dev/null	

cv_full.ps: cv_full.dvi
	dvips -o $@ $<

cv_full.dvi: $(texlist)
	latex cv_full.tex
	latex cv_full.tex

.PHONY: clean

clean:
	@rm *.dvi *.pdf *.ps *.log *.toc *.aux *.out *.idx *.ilg *.ind *.spl *.bbl *.blg -f >& /dev/null
	@$(info All unnecessary makefile dependencies have been removed!)
