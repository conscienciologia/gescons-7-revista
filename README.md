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

find . -type f -iname "\*.png" \
 | parallel --bar 'convert "{}" -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" "{= s/\.png$/.pdf/ =}"'

convert articles/atualizacoes/fotos/materia5/Instagram-Editares.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" "articles/atualizacoes/fotos/materia5/Instagram-Editares.pdf"

convert articles/capa_atualizacoes.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" capa_atualizacoes.jpg
convert articles/capa_entrevistas.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" capa_entrevistas.jpg
convert articles/capa_parcerias.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" capa_parcerias.jpg
convert articles/capa_resumo.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" capa_resumo.jpg
convert articles/fundo-generico.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" fundo-generico.jpg

convert articles/capa_atualizacoes.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" articles/capa_atualizacoes.pdf
convert articles/capa_atualizacoes.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" articles/capa_atualizacoes.jpg
convert articles/capa_entrevistas.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" articles/capa_entrevistas.jpg
convert articles/capa_parcerias.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" articles/capa_parcerias.jpg
convert articles/capa_resumo.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" articles/capa_resumo.jpg
convert articles/balanco/grafico/grafico.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" articles/balanco/grafico/grafico.jpg
convert capa/capa.pdf -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" capa/capa.jpg

images/AIEC-Logo-1024x364.png images/AIEC-Logo-1024x364.png
images/Arace-Logo-1024x764.png images/Arace-Logo-1024x764.png
images/Assipi-Logo-3-1024x371.png images/Assipi-Logo-3-1024x371.png
images/cover.png images/cover.png
images/Embaixada-da-Paz-150x150.png images/Embaixada-da-Paz-150x150.png
images/ISIC-Logo-946x1024.png images/ISIC-Logo-946x1024.png
images/Logo-ASSINVEXIS-Escura-1024x220.png images/Logo-ASSINVEXIS-Escura-1024x220.png
images/logo-LIDERARE-2-1024x1024.png images/logo-LIDERARE-2-1024x1024.png
images/Logo-OIC-1024x567.png images/Logo-OIC-1024x567.png
images/logo_ceaec.png images/logo_ceaec.png
images/Orthocognitivus-LOGOMARCA-1024x365.png images/Orthocognitivus-LOGOMARCA-1024x365.png
images/UNICIN-nova-LOGO-02-300x117.png images/UNICIN-nova-LOGO-02-300x117.png
images/UNIESCON-2048x1741.png images/UNIESCON-2048x1741.png

convert images/Unicin-Logo-1024x315.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" images/Unicin-Logo-1024x315.pdf
convert images/Logo-UNIESCON-2048x1741.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" images/Logo-UNIESCON-2048x1741.pdf
convert images/IIPC_logo.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" images/IIPC_logo.pdf
convert images/Logo-Editares-com-Marca-Registrada.png -colorspace CMYK -profile "profiles/Coated_Fogra39L_VIGC_300.icc" images/Logo-Editares-com-Marca-Registrada.pdf
