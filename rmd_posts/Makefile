MDS := $(patsubst %.Rmd,%.md,$(wildcard *.Rmd))
POSTDIR := ../_posts

unexport HOME

all: $(MDS) 

%.md: %.Rmd
	Rscript -e "source('knit_it.R'); knit_it('$<')"
	cp $@ ../_posts/.
