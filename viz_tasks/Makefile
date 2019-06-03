# Create challenge.Rmd and solution.Rmd files from master.Rmd file
#
# Usage:
# % make              # Create challenge.Rmd and solution.Rmd files
# % make clean        # Remove challenge.Rmd and solution.Rmd files

# Authors: Zach del Rosario, Bill Behrman
# Version: 2018-05-17

MASTER = master
SOLUTION = solution
CHALLENGE = challenge

all: ${SOLUTION}.Rmd ${CHALLENGE}.Rmd

grid:
	pdflatex grid.tex

${SOLUTION}.Rmd: ${MASTER}.Rmd
	sed -E \
	-e '/<!-- task-begin -->/,/<!-- task-end -->/d' \
	-e '/# task-begin/,/# task-end/d' \
	-e '/# solution-(begin|end)/d' \
	-e '/<!-- solution-(begin|end)/d' \
	< $< > $@
	Rscript -e "rmarkdown::render('${SOLUTION}.Rmd')"

${CHALLENGE}.Rmd: ${MASTER}.Rmd
	sed -E \
	-e 's/^author:.*|.*# yaml-author.*/author: \"Your Name\"/' \
	-e 's/^date:.*/date: /' \
	-e '/<!-- solution-begin -->/,/<!-- solution-end -->/d' \
	-e '/# solution-begin/,/# solution-end/d' \
	-e '/# task-(begin|end)/d' \
	-e '/<!-- task-(begin|end)/d' \
	< $< > $@
	Rscript -e "rmarkdown::render('${CHALLENGE}.Rmd')"

clean:
	rm -f ${CHALLENGE}.Rmd ${SOLUTION}.Rmd
	rm -f grid.aux
