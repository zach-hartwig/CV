texlist := $(wildcard *.tex)

TARGET := ZachHartwig_CV_Short.pdf

$(TARGET): cv_short.ps
	ps2pdf $< $@
	@rm *.dvi *.ps *.log *.toc *.aux *.out *.idx *.ilg *.ind *.spl *.bbl *.blg -f >& /dev/null	

cv_short.ps: cv_short.dvi
	dvips -o $@ $<

cv_short.dvi: $(texlist)
	latex cv_short.tex
	latex cv_short.tex

.PHONY: clean

clean:
	@rm *.dvi *.pdf *.ps *.log *.toc *.aux *.out *.idx *.ilg *.ind *.spl *.bbl *.blg -f >& /dev/null
	@$(info All unnecessary makefile dependencies have been removed!)
