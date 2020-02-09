# Expressões Regulares (Continuação)

### <b>Sequências especiais</b>
Uma sequência especial inicia como uma **barra (\)** seguida por um dos caracteres da lista abaixo e tem um significado especial: <br>
![funcao](/imagens/regex1.png)

Exemplos:
``` python
import re

txt = "chove chuva chove sem parar"

#Retorna a string ch se estiver no início da frase(retorna apenas 1:

x = re.findall("\Ach", txt)

print('x1 = ',x)
```
**Resultado:**<br>
x1 =  ['ch']<br>

``` python
import re

txt = "chove chuva chove sem parar"

#retorna a string  ch se estiver no início das palavras(retorna apenas 1:

x = re.findall(r"\bch", txt)

print('x2 = ',x)
```
**Resultado:**<br>
x2 =  ['ch', 'ch', 'ch']<br>

``` python
import re

txt = "chove chuva chove sem parar"

#Retorna a string ch se estiver no fim das palavras(retorna apenas 1:

x = re.findall(r"ch\b", txt)

print('x3 = ',x)
```
**Resultado:**<br>
x3 =  [] <br>

``` python
import re

txt = "chove chuva chove sem parar"

#Retorna a string "ch", se estiver presente, mas NÃO no início da palavra:

x = re.findall(r"\Bch", txt)

print('x4 = ',x)

#Retorna a string "ch" se estiver presente, mas NÃO no fim da palavra:

x = re.findall(r"ch\B", txt)

print('x4 = ',x)
```
**Resultado:**<br>
x4 =  []<br>
x4 =  ['ch', 'ch', 'ch']<br>

``` python
import re

txt = "chove chuva chove sem parar"

#Retorna os caracteres dígitos(números de 0-9), se existir

x = re.findall(r"\d", txt)

print('x5 = ',x)
```
**Resultado:**<br>
x5 =  [] <br>

``` python
import re

txt = "chove chuva chove sem parar"

#Retorna os caracteres NÃO dígitos(números de 0-9), se existir

x = re.findall(r"\D", txt)

print('x6 = ',x)
``` 
**Resultado:**<br>
x6 =  ['c', 'h', 'o', 'v', 'e', ' ', 'c', 'h', 'u', 'v', 'a', ' ', 'c', 'h', 'o', 'v', 'e', ' ', 's', 'e', 'm', ' ', 'p', 'a', 'r', 'a', 'r'] <br>

``` python
import re

txt = "chove chuva chove sem parar"

#Retorna apenas os espaços em branco, se existir
x = re.findall("\s", txt)
print('x7 = ',x)
```
**Resultado:**<br>
x7 =  [' ', ' ', ' ', ' ']<br>

``` python
import re

txt = "chove chuva chove sem parar"

#Retorna os caracteres, mas NÃO os espaços em branco,  se existir
x = re.findall("\S", txt)
print('x8 = ',x)
```
**Resultado:**<br>
x8 =  ['c', 'h', 'o', 'v', 'e', 'c', 'h', 'u', 'v', 'a', 'c', 'h', 'o', 'v', 'e', 's', 'e', 'm', 'p', 'a', 'r', 'a', 'r'] <br>

``` python
import re

txt = "chove chuva chove sem parar"

#Retorna a sequência, se terminar a frase, isto é, se está no final":

x = re.findall("arar\Z", txt)

print('x9 = ',x)
```
**Resultado:**<br>
x9 =  ['arar'] <br>
