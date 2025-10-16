Como gerar o PDF da revista

clean

> latexmk -c main.tex

build:

> latexmk -f -pdf -shell-escape -file-line-error -interaction=nonstopmode main.tex

Ou:

> latexmk -c main.tex & latexmk -f -pdf -shell-escape -file-line-error -interaction=nonstopmode main.tex

Controle de

articles/\*_/_.tex
