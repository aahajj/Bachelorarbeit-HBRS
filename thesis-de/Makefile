.PHONY:clean tidy
all:
	make main.pdf

main.pdf: main.tex lit/*.bib section/*.tex 
	xelatex -synctex=1 main.tex
	biber main
	xelatex -synctex=1 main.tex
	xelatex -synctex=1 main.tex

clean:
	make tidy
	rm -f main.pdf

tidy:
	find . -name "*.aux" | xargs rm -f
	rm -f *.bbl *.log *.out *.idx *.toc *.blg *.width *.synctex.gz *.bcf *.run.xml *.lof *.lot
