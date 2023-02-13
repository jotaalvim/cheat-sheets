A arte de editar um ficheiro está em saber mexer o ponteiro

# ficheiro de configuração
    • ~/.vimrc

# Modo comando 
	:      entrar no 
## Selecionar blocos de código para aplicar comandos
	:%     para todas as linhas
	:20,50 entre as linhas 20 e 50
	:20,$  entre as linhas 20 e fim
	:20,.  entre as linhas 20 e linha atual

### Nas substituições
Em vim usas-se na maioria expressões [[Regex]] mas algumas coisas ficam diferentes
* substituição \\n usa-se o \\r 
* \\v - very magical serve para ajudar com os parêntesis e.g. para fazer swap a 2 palavras  em vim puro:```
```
s/\(\w\+\) \(\w\+\)/\2 \1/
```
Com o uso do \\v fica muito mais limpo de ler
```
s/\v(\w+) (\w+)/\2 \1/
```

C-P em modo insert - completa palavras (Acho que tenho um plugin para isto?)
<C-X> <C-Y>
<C-E>move camera para baixo
<C-Y> move camera para cima

Contas o número de vezes que uma palavra ocorre
    :%s/palavra//gn
    n -> diz para não fazer a substituição

:%s/.*/<a>&<\/a>/
:%norm i<a>
:%norm A</a>

v - modo visual
<C-V> seleciona bloco

K -> manual

---
Status: #cheat-sheets
Tags: [[Programming]]