PROJECT_NAME = cfa_notes
PDF          = $(PROJECT_NAME).pdf
REQUIRE      = $(PROJECT_NAME).tex $(wildcard chapters/*.tex)
TEMP         = $(PROJECT_NAME).{aux,log,idx,out,toc}

TEX          = xelatex
MODE         = -interaction=nonstopmode
MAKEIDX      = makeindex

.PHONY: ALL install clean distclean

ALL: $(PDF)

$(PDF): $(REQUIRE)
	$(TEX) $(MODE) $(PROJECT_NAME).tex
	#$(MAKEIDX) -s $(PROJECT_NAME).idx $(PROJECT_NAME)
	$(TEX) $(MODE) $(PROJECT_NAME)

install: ALL
	mv $(PDF) ..

clean:
	$(RM) $(PROJECT_NAME).aux $(PROJECT_NAME).log $(PROJECT_NAME).idx $(PROJECT_NAME).out $(PROJECT_NAME).toc

distclean: clean
	$(RM) $(PDF)

