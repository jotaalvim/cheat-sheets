# uniq 
	report or omit repeated lines
    -c  conta linhas adjacentes iguais
    podes dar jeito usar com o sort

# grep
    -r - recursivo
    -w - palavras inteiras
    -i - ignore case, maiúsculas e minúsculas
	-o - devolve só o que foi match
	-P - perl notation
	-c - conta numero de ocorrencias
    grep M myheart.csv | grep -P -c '1\s*$'
	

# awk
	awk -F, '$2 == "M" {a++} END {print a}' myheart.csv
	awk -F, '$2 == "M" {a+=$6} END {print a}' myheart.csv

# pandoc
    conversor entre formatos
    pandoc input.abc -t beamer -o output.pdf

# links simbolicos
	ln -s /home/jotaalvim/Documents/projetos/jotaalvim-tools/ddl ~/.local/bin/ddl
 
# pushd
	garda uma dir

# popd
	volta a dir

# sort
    ordena
    -n → ordena numéricamente

# locate
    procura um ficheiro
    atualiza diariamente

# find
    dá todos os ficheiros de uma dir recursivamente





# todo 
# feh  
	da para ver diretoria ,imagens

# pdftotext
    -layout

# pdfimages -png

# pdftohtml

# pv
    mostra as coisas como se estivesse a escrever em tempo real
    pv -qL 10

---
# Status:
#cheat-sheets
# Tags: [[Programming]]
