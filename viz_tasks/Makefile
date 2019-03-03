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

${SOLUTION}.Rmd: ${MASTER}.Rmd
	sed -E \
	-e '/<!-- task-begin -->/,/<!-- task-end -->/d' \
	-e '/# task-begin/,/# task-end/d' \
	-e '/# solution-(begin|end)/d' \
	-e '/<!-- solution-(begin|end)/d' \
	< $< > $@

${CHALLENGE}.Rmd: ${MASTER}.Rmd
	sed -E \
	-e 's/^author:.*|.*# yaml-author.*/author: \"Your Name\"/' \
	-e 's/^date:.*/date: 2018-/' \
	-e '/<!-- solution-begin -->/,/<!-- solution-end -->/d' \
	-e '/# solution-begin/,/# solution-end/d' \
	-e '/# task-(begin|end)/d' \
	-e '/<!-- task-(begin|end)/d' \
	< $< > $@

clean:
	rm -f ${CHALLENGE}.Rmd ${SOLUTION}.Rmd
