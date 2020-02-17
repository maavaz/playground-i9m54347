# Expressões Regulares (Continuação)

### <b>Metacaracteres</b>

Metacaracteres corresponde a um conjunto de caracteres que possuem um signficado expecífico e que são interpretados de maneira especial pelo mecanismo RegEx:

![regex](/imagens/regex.png)
 
### <b> Caracter [] </b>
Os colchetes permitem a inserção de um conjunto de caracteres que se deseja procurar uma correspondência. Dentro dos colchetes são colocadaos os caracteres permitidos para a correspondência.
``` python
import re
padrao = 'n[ãa]o'
texto='não é bom decorar os comandos, mas não decorar torna difiícil memorizar. nao deixe de estudar'

#Procurar os caracteres "r,s,t" no texto e retorna uma lista.
resultado = re.findall(padrao, texto) 

print('Resultado: ', resultado)
``
**Resultado:**  ['não', 'não', 'nao']

###Outro Exemplo:
``` python
import re
padrao = '[rst]'
texto='Bom programador? ler e interpretar textos aprender conceitos, não decorar comandos e fazer muitos exercícios'

#Procurar os caracteres "r,s,t" no texto e retorna uma lista.
resultado = re.findall(padrao, texto) 

print('Resultado: ', resultado)
```
**Resultado:** 
['r', 'r', 'r', 'r', 't', 'r', 'r', 't', 'r', 't', 't', 's', 'r', 'r', 't', 's', 'r', 'r', 's', 'r', 't', 's', 'r', 's']

O padrão **[rst]** irá retornar uma lista contendo os caracteres **r, s, t**. <br>
Em vez de digitar toda a sequência, pode-se especificar o intervalo utilizando o caracter **hífen (-)** para separar os caracteres de inícios e fim, por exemplo:<br>
<b>[r-t]  = [rst] <br>
[1-3]  = [123]  <br>
[0-27] = [0127] </b><br>

O caracter **^** funciona como a negação da sequência informada se for colocado no início da sequência entre colchetes: <br>
<b>[^abc]</b> significa qualquer caracter com exceção de a, b ou c. <br>
<b>[^0-9]</b> significa qualquer caracter não-dígito. <br>

``` python
import re 

padrao  = '[k-o]' #Seleciona os caracteres k, l, m, n, o
padrao1 = '[0-25]' #Seleciona os dígitos: 0, 1, 2, 5
padrao2 = '[^0-9 a-z]' #Seleciona os caracteres com exceção dos dígitos de 0 até 9 e letras de a até z minusculos

texto='A previsão para os próximos 30 dias é de min de 15 graus e max 25 graus'
resultado = re.findall(padrao, texto) 
print('resultado: ', resultado)
resultado = re.findall(padrao1, texto) 
print('resultado1: ', resultado)
resultado = re.findall(padrao2, texto) 
print('resultado2: ', resultado)
```
**Resultado:**
resultado:  ['o', 'o', 'm', 'o', 'm', 'n', 'm'] <br>
resultado1:  ['0', '1', '5', '2', '5'] <br>
resultado2:  ['A', 'ã', 'ó', 'é'] <br>

### <b> Caracteres ^ . $ </b>
Esses caracteres já apresentados em exemplo anterior, significam: <br>
- **^** (o caracter seguinte ao símbolo deve iniciar a sequência) <br>  
- **.** (qualquer caracter substitui o ponto) <br>
- **$** (a sequência de terminar com o caracter anterior ao símbolo) <br>
Por exemplo: no padrão **'^m...o$'** aplicado sobre as palavras **['amarco', 'marcondes', 'amacro', 'masco']**, o método de pesquisa **findall()** só encontra equivalência na última string, pois é a única que inicia com **m** e termina com **o** e há 3 caracteres entre eles.

### <b> Caracteres * + {} |</b>
Esses caracteres possuem os seguintes significados: <br>
- <b>*</b> (o caracter anterior ao símbolo pode não ocorrer ou ter mais de uma ocorrência) <br>  
- **+**  (o caracter anterior ao símbolo deve ter pelo menos uma ocorrência ) <br>
- **{}** (o caracter anterior as chaves deve ter o número de ocorrências especificadas dentro das chaves) <br>
- **|**  (um ou outro caracter ou sequência, ou os dois devem ocorrer na pesquisa) <br> 
``` python
import re
txt = "Deu um abraço no laço mas alegou cansaço na carcaça para caça "

#verifica se a string contém "aç" seguido de 0 ou mais caracteres "a":

x = re.findall("aça*", txt)

print("x1 = ", x)

#verifica se a string contém "aç" seguido de 1 ou mais caracteres "a":

x = re.findall("aça+", txt)

print("x2 = ", x)

txt = "compromisso de acesso ao abcesso onde o tratamento foi sucesso"
#verifica se a string contém "es" contém necessariamento 2 caracteres "s":

x = re.findall("es{2}", txt)

print("x3 = ", x)

#verifica se a string contém "abc" ou "ess" ou os dois:
x = re.findall("abc|ess", txt)

print("x4 = ", x)
```
**Resultados:** <br>
x1 =  ['aç', 'aç', 'aç', 'aça', 'aça'] <br>
x2 =  ['aça', 'aça'] <br>
x3 =  ['ess', 'ess', 'ess'] <br>
x4 =  ['ess', 'abc', 'ess', 'ess'] <br>

### <b> Caractere ()</b>
Parênteses são usados para agrupar sub-padrões. Por exemplo:Desejamos retornar os caracteres "a" ou "e" ou "i" que esteja seguidos de "st"<br>
``` python
import re
sentenca = 'avistamos estáticos o elastico e o plastico'

#retorna qualquer sequência a ou e ou i seguido de st

resultado = re.findall(r'(a|e|i)st', sentenca)
print(matched)
```
**Resultado:***<br>
['i', 'e', 'a', 'a']
