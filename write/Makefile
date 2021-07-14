# vim: set ts=8 sts=0 sw=8 si fenc=utf-8 noet:
# vim: set fdm=marker fmr={{{,}}} fdl=0 foldcolumn=4:
#
.PHONY: all clean

imgdir := input/img
header := src/header.html
css    := src/github.css

images := $(shell find $(imgdir) -type f)
data := input/segment-layout-data.parquet input/table.parquet

all: output/blogpost.html

clean: 
	-rm -r output/*

output/%.html: src/%.Rmd src/header.html src/github.css $(images) $(data)
	-mkdir output
	cp $< output/
	cp $(header) output/
	cp $(css) output/
	cp -r $(imgdir) output/
	Rscript -e "rmarkdown::render('output/$*.Rmd')"
	-rm output/$*.Rmd
	-rm output/*chunk*.png
	-rm output/$*.md
	-rm -r output/img
	-rm output/header.html
	-rm output/github.css

