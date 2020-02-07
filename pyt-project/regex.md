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
**Resultado:** <br>
Encontrei !!<br>
Encontrei !!<br>
Não encontrei !!<br>
Encontrei !!<br>

Outros métodos de pesquisa:
   ![import](/imagens/metodos.png)
   
Pesquisar as ocorrências da string 'ma' no texto do exemplo (utilizamos um **r** na frente da string para tratarmos como uma string raw (caracteres seguidos por barra invertida não tem significado especial). 
   
``` python
padrao = r'ma'     #Procurar a string ma  
texto = r"marco, vamos fazer um teste. Primeiro \nmarco as palavras e depois envio ao marcondes o texto qua irá amassar o texto"
#Retorna a lista com todas sequencias ma encontadas
saida = re.findall(padrao, texto)
print('saida1: ',saida)

#Usando o método search que procura a sequencia 'ma' em qualquer parte do texto
saida = re.search(padrao, texto)
print('saida2: ',saida)
print('saida3: ',saida[0])
 
```
**Resultado:** <br> 
Saida 1: ['ma', 'ma', 'ma', 'ma']
Saida 2: <_sre.SRE_Match object; span=(0, 2), match='ma'>
Saida 3: ma


