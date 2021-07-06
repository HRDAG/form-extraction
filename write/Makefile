# vim: set ts=8 sts=0 sw=8 si fenc=utf-8 noet:
# vim: set fdm=marker fmr={{{,}}} fdl=0 foldcolumn=4:
#
.PHONY: all clean

imgdir := input/img

all: output/blogpost.html

clean: 
	-rm -r output/*

output/%.html: src/%.Rmd
	-mkdir output
	cp $< output/
	cp -r $(imgdir) output/
	Rscript -e "rmarkdown::render('output/$*.Rmd')"
	-rm output/$*.Rmd
	-rm output/*chunk*.png
	-rm output/$*.md
	-rm -r output/img

