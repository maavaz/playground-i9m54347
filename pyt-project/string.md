# Manipulando String em Python

A melhor maneira de manipular sequências de caracteres (Strings) em python é através de seus métodos. A seguir, apresentamos os principais métodos em Strings:
        ![string](/imagens/string1.png)

``` python
subs = 'os'
texto='Bom programador? ler e interpretar textos\n aprender conceitos, não decorar comandos.\nPor fim, fazer muitos exercícios'

#conta quantas vezes aparece a string 'os' no texto
conta = texto.count(subs)
print('quantidade de os = ', conta)
```
**Resultado:** <br>
quantidade de os =  5<br>

``` python
subs='amador'

#procura pela substring aramzenada em subs e retorna a posição inicial encontrada
posicao = texto.find(subs)

print('posição inicial da substring \"{0}\" no Texto = {1}'.format(subs,posicao))
```
**Resultado:** <br>

posição inicial da substring "amador" no Texto = 21 <br>

``` python
texto1= ('Linguagem', 'de', 'programação', 'Python')
espaco = ' '

#Concatena o caracter espaço com entre as strings de texto1
texto2 = espaco.join(texto1)

print(texto2)
```
**Resultado:** <br>

Linguagem de programação Python <br>

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

``` python
texto1 = 'A caixa 1 é azul, A caixa 2 é verde e caixa 3 é vermelha'

#Substitui a string caixa por lata em texto1
texto2 = texto1.replace('caixa', 'lata')

print(texto2)

```
**Resultado:** <br>

A lata 1 é azul, A lata 2 é verde e lata 3 é vermelha
