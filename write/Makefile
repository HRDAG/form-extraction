# vim: set ts=8 sts=0 sw=8 si fenc=utf-8 noet:
# vim: set fdm=marker fmr={{{,}}} fdl=0 foldcolumn=4:
#
.PHONY: all clean

all: output/blogpost.html

clean: 
	-rm -r output/*

output/%.html: src/%.Rmd
	-mkdir output
	Rscript -e "rmarkdown::render('$<')"
	mv src/$*.html $@
	-rm src/$*.md

