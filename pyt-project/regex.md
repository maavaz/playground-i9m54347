# Expressões Regulares

Expressões regulares (chamadas REs, ou regexes ou padrões regex) são definidas como sequências de caracteres que definem um padrão de pesquisa especializada. Na computação, as expressões regulares fornece uma descrição concisa e flexível para encontrar correspondências de cadeias de texto, como caracteres, palavras ou padrões de caracteres. Um expressão regular, incluída na linguagem Python e, disponível através do módulo re, é escrita em uma linguagem formal que pode ser interpretado por um processador de expressão regular. 
Nos programas python, para se usar expressões regulares expressions é necessário a utilização da biblioteca (pacote) **re**.   
                        ![import](/imagens/re.png)


Suponha a seguinte expressão: **^m...o$** <br>
O código acima define um padrão RegEx que significa: **qualquer sequência de cinco letras começando com m e terminando com o.**
Esse padrão pode ser confrontado com sequências de caracteres e verificar se ele é encontrado na sequência, como no código abaixo:
``` python 	         
import re
frases = ['marco', 'marcondes', 'macro', 'masco']
padrao = '^m...o$'
# match encontra equivalência apenas se o padrão ocorrer no início da string e com o mesmo número de carcateres
for palavra in frases:
    resultado = re.match(padrao, palavra)  
    if resultado:
        print("Encontrei !!")
    else:
        print("Não encontrei !!")
```
**Resultado:** <br>
Encontrei !!  <br>
Não encontrei !!  <br>
Encontrei !!  <br>
Encontrei !!  <br>

Alguns métodos de pesquisa:<br> 
   ![import](/imagens/metodos.png)
 
### <b>Método findall()</b>   
Pesquisar as ocorrências da string 'ma' no texto do exemplo (utilizamos um **r** na frente da string para tratarmos como uma string raw (caracteres seguidos por barra invertida não tem significado especial). 
   
``` python
import re
padrao = r'ma'     #Procurar a string "ma"  
texto = r"marco, vamos fazer um teste. Primeiro \nmarco as palavras e depois envio ao marcondes o texto qua irá amassar o texto"

#Retorna a lista com todas sequencias "ma" encontadas
saida = re.findall(padrao, texto)
print('saida1: ',saida)
```
**Resultado:** <br> 
Saida 1: ['ma', 'ma', 'ma', 'ma'] <br> 

### <b>Método search()</b>
```python
#Usando o método search que procura a sequencia 'ma' em qualquer parte do texto
saida = re.search(padrao, texto)
print('saida2: ',saida)
print('saida3: ',saida[0])
```
**Resultado:** <br> 

Saida 2: <_sre.SRE_Match object; span=(0, 2), match='ma'> <br> 
Saida 3: ma <br> 

### <b>Método finditer()</b>
```python
#Retorna as tuplas com as posições de cada ocorrência no texto
saida = re.finditer(padrao,texto)

for match in saida:
    print('Saida4: ', match.span())
 
```
**Resultado:** <br> 

Saida4:  (0, 2) <br> 
Saida4:  (40, 42) <br> 
Saida4:  (76, 78) <br> 
Saida4:  (103, 105) <br> 

Outros dois métodos:
  ![import](/imagens/metodos1.png)

### <b>Método split()</b>

``` python
import re

padrao = 'os'      
texto = r"aos poucos vamos entendendo os diferentes métodos" 

#divide o texto numa lista de acordo com o padrão
saida = re.split(padrao, texto)
i = 1
for pedaco in saida:
    print("Split {0}: {1}".format(i, pedaco))
    i+=1 
```
**Resultado:** <br>
Split 1: a <br>
Split 2:  pouc <br>
Split 3:  vam <br>
Split 4:  entendendo <br> 
Split 5:  diferentes métod <br>
Split 6: <br>

### <b>Método sub()</b>

``` python
origem = 'diferentes'     
subst ="vários"

#Substitui a string em origem pela string em subst
saida =re.sub(origem, subst, texto)

print('Antes: ', texto)
print("Depois: ", saida)
```
**Resultado:** <br>

Antes:  aos poucos vamos entendendo os diferentes métodos <br>
Depois:  aos poucos vamos entendendo os vários métodos

