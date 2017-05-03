# Makefile
PDFC=latex
FILENAME=ctgen_weight
DVI = dvips

SOURCE=$(FILENAME).tex
FILES=
#FILES=acmsmall.cls algorithm2e.sty  IEEEabrv.bib ctgen_weight.bib

#TMP=$(FILENAME).aux $(FILENAME).log $(FILENAME).dvi $(FILENAME).ps

TMP=$(FILENAME).aux $(FILENAME).log $(FILENAME).bbl $(FILENAME).blg $(FILENAME).dvi $(FILENAME).ps $(FILENAME).out # $(FILENAME).spl
#ALL: $(SOURCE) $(FILES)
#	$(PDFC) $(SOURCE)
#	$(PDFC) $(SOURCE)
#	$(DVI) $(FILENAME).dvi
#	ps2pdf $(FILENAME).ps

ALL: $(SOURCE) $(FILES)
	$(PDFC) $(SOURCE)
	bibtex $(FILENAME)
	$(PDFC) $(SOURCE)
	$(PDFC) $(SOURCE)
	$(PDFC) $(SOURCE)
	dvips $(FILENAME).dvi
	ps2pdf $(FILENAME).ps
read:
	evince $(FILENAME).pdf &

clean:
	-rm $(TMP)

distclean: clean
	-rm $(FILENAME).pdf
