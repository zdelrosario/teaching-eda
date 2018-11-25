SHELL := /bin/bash
filename=handout

pdf: 
	pdflatex ${filename}
	bibtex ${filename}||true
	pdflatex ${filename}
	pdflatex ${filename}

quick:
	pdflatex ${filename}

clean:
	rm -f ${filename}.{log,aux,out,bbl,blg,fls,ilg,nlo,nls}
	rm -f ${filename}.{fdb_latexmk,stderr.log,stdout.log,tex.swp}

links:
	# Macros
	cp -f ~/Git/zachs_macros/zachs_macros.tex zachs_macros.tex
	cp -f ~/Git/zachs_macros/numdef.sty numdef.sty
