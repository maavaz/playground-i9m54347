# Expressões Regulares

Expressões regulares (chamadas REs, ou regexes ou padrões regex) são definidas como sequências de caracteres que definem um padrão de pesquisa especializada. Na computação, as expressões regulares fornece uma descrição concisa e flexível para encontrar correspondências de cadeias de texto, como caracteres, palavras ou padrões de caracteres. Um expressão regular, incluída na linguagem Python e, disponível através do módulo re, é escrita em uma linguagem formal que pode ser interpretado por um processador de expressão regular. 
Nos programas python, para se usar expressões regulares expressions é necessário a utilização da biblioteca (pacote) **re**.   
                        ![import](/imagens/re.png)


Suponha a seguinte expressão: **^m...o$**
O código acima define um padrão RegEx que significa: qualquer sequência de cinco letras começando com **m** e terminando com **o**.
Esse padrão pode ser confrontado com sequências de caracteres e verificar se ele é encontrado na sequência, como no código abaixo:
``` python 	         
import re
frases = ['marco', 'macro', 'Marco', 'masco']
padrao = '^m...o$'

for palavra in frases:
    result = re.match(padrao, palavra)
    if result:
        print("Encontrei !!")
    else:
        print("Não encontrei !!")
```
Resultado: <br>
Encontrei !!<br>
Encontrei !!<br>
Não encontrei !!<br>
Encontrei !!<br>


        
