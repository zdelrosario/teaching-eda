SOURCE = slides
WRITE = seeme_slides

main:
	Rscript -e 'rmarkdown::render("${SOURCE}.Rmd")'
	mv ${SOURCE}.html ${WRITE}.html

all:
	Rscript -e 'rmarkdown::render("${SOURCE}.Rmd", output_format = "all")'
	mv ${SOURCE}.html ${WRITE}.html
	mv ${SOURCE}.pdf ${WRITE}.pdf

clean:
	rm ${WRITE}.html
