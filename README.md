Como gerar o PDF da revista

clean

> latexmk -c main.tex

build:

> latexmk -f -pdf -shell-escape -file-line-error -interaction=nonstopmode main.tex

Ou:

> latexmk -c main.tex & latexmk -f -pdf -shell-escape -file-line-error -interaction=nonstopmode main.tex

ou

> texfile=main.tex
> latexmk -c $texfile & latexmk -f -pdf -shell-escape -file-line-error -interaction=nonstopmode $texfile

Controle de

articles/\*_/_.tex

# CMYK

https://tex.stackexchange.com/questions/9961/pdf-colour-model-and-latex/9973#9973
