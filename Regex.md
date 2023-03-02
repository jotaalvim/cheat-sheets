## Expressões Regulares
    & → aquilo que fez matching na expressão regular
    . → 1 carater != de \n
    * → 0 ou mais occorencias do que está a esquerda
    + → 1 ou mais occorencias do que está a esquerda
    [a-zA-Z0-9] → conjunto de alfanumerico
    \w → conjunto     alfanumerico
    \W → conjunto NAO alfanumerico
    \d → digito
    \D → NAO digito
    ^ → inicio da linha
    $ → fim da linha
    ^ → [^abc] não a,b ou c
    {2} → repetiçao do padrao 2 vezes
    {1,5} → repetiçao do padrao 1 vezes até 5 vezes
    \s → whitespace
    \S → NAO whitespace

	\b → dá match com uma string de comprimento 0 wordboundary 

### TODO 
* negative/positive look ahead 


### Exercício
String binária que contém pelo menos tres 1
```
(0|1)*1(0|1)*1(0|1)*1(0|1)*
```
### Não contem a substring 110
---
Status:
#cheat-sheets
Tags: [[Programming]] - [[Processamento-Linguagens]]