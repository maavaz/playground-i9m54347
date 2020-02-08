# Manipulando String em Python

A melhor maneira de manipular sequências de caracteres (Strings) em python é através de seus métodos. A seguir, apresentamos os principais métodos em Strings:
        ![string](/imagens/string1.png)
### <b> Método count() </b>
``` python
subs = 'os'
texto='Bom programador? ler e interpretar textos aprender conceitos, não decorar comandos e fazer muitos exercícios'

#contar a quantidade de vezes que aparece a string 'os' no texto
conta = texto.count(subs)
print('quantidade de os = ', conta)
```
**Resultado:** <br>
quantidade de os =  5<br>

### <b> Método find() </b>
``` python
subs='amador'

#procura pela substring aramzenada em subs e retorna a posição inicial encontrada
posicao = texto.find(subs)

print('posição inicial da substring \"{0}\" no Texto = {1}'.format(subs,posicao))
```
**Resultado:** <br>

posição inicial da substring "amador" no Texto = 21 <br>

### <b> Método join() </b>
``` python
texto1= ('Linguagem', 'de', 'programação', 'Python')
espaco = ' '

#Concatena o caracter espaço com entre as strings de texto1
texto2 = espaco.join(texto1)

print(texto2)
```
**Resultado:** <br>

Linguagem de programação Python <br>

### <b> Método strip() </b>
``` python
txt = "     Python     "

#Remove os caracteres (padrão espaços) do início e fim.as funções lstrip() e rstrip() removem a esquerda ou a direita somente 
x = txt.strip()

print("De todas as Linguagens", x, "é a minha favorita")

txt = ",,,,,Python....argh"

x = txt.strip(',.argh')
print("De todas as Linguagens", x, "é a minha favorita")
```
**Resultado:** <br>

De todas as Linguagens Python é a minha favorita <br>

De todas as Linguagens Python é a minha favorita <br>

### <b> Método replace() </b>
``` python
texto1 = 'A caixa 1 é azul, A caixa 2 é verde e caixa 3 é vermelha'

#Substitui a string caixa por lata em texto1
texto2 = texto1.replace('caixa', 'lata')

print(texto2)

```
**Resultado:** <br>

A lata 1 é azul, A lata 2 é verde e lata 3 é vermelha

### <b> Método split() </b>
``` python
texto1 = 'C,Python,C++,Java,JavaScript,VBA'

#Quebra o texto no separador vírgula.
linguagens = texto1.split(',')
for i in linguagens:
    print(i)
```
**Resultado:** <br>
C<br>
Python<br>
C++<br>
Java<br>
JavaScript<br>
VBA<br>

