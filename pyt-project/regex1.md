# Expressões Regulares (Continuação)

### <b>Metacaracteres</b>
Metacaracteres corresponde a um conjunto de caracteres que possuem um signficado expecífico e que são interpretados de maneira especial pelo mecanismo RegEx:

![regex](/imagens/regex.png)

### <b> Caracter [] </b>
---
``` python

padrao = '[rst]'
texto='Bom programador? ler e interpretar textos aprender conceitos, não decorar comandos e fazer muitos exercícios'

#Procurar os caracteres "r,s,t" no texto e retorna uma lista.
resultado = re.findall(padrao, texto) 

print('Resultado: ', resultado)
```
**Resultado:** 
['r', 'r', 'r', 'r', 't', 'r', 'r', 't', 'r', 't', 't', 's', 'r', 'r', 't', 's', 'r', 'r', 's', 'r', 't', 's', 'r', 's']

O padrão **[rst]** irá retornar uma lista contendo os caracteres **r, s, t**. <br>
Pode-se especificar o intervalo utilizando o caracter hífen **-** para serar os extremos, por exemplo:<br>
[r-t]  = [rst] <br>
[1-3]  = [123]  <br>
[0-27] = [0127] <br>

O caracter **^** funciona como a negação da sequência informada se for colocado no início sa sequência entre colchetes: <br>
[^abc] significa qualquer caracter com exceção de a, b ou c.
[^0-9] significa qualquer caracter não-dígito.

``` python
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
---
Esses caracteres já apresentados em exemplo anterior, significam: <br>
- **^** (o caracter seguinte ao símbolo deve iniciar a sequência) <br>  
- **.** (qualquer caracter substitui o ponto) <br>
- **$** (a sequência de terminar com o caracter anterior ao símbolo) <br>
Por exemplo: no padrão **'^m...o$'** aplicado sobre as palavras ['amarco', 'marcondes', 'amacro', 'masco'], o método de pesquisa **findall()** só encontra equivalência na última string, pois é a única que inicia com **m** e termina com **o** e há 3 caracteres entre eles.

### <b> Caracteres * + {} </b>
---
Esses caracteres possuem os seguintes significados: <br>
- <b>*</b> (o caracter anterior ao símbolo pode não ocorrer ou ter mais de uma ocorrência) <br>  
- **+** (o caracter anterior ao símbolo deve ter pelo menos uma ocorrência ) <br>
- **{}** (o caracter anterior as chaves deve ter o número de ocorrências especificadas dentro das chaves) <br>
``` python
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
```
**Resultados:** <br>
x1 =  ['aç', 'aç', 'aç', 'aça', 'aça'] <br>
x2 =  ['aça', 'aça'] <br>
x3 =  ['ess', 'ess', 'ess'] <br>


