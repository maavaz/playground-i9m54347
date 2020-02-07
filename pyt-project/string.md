# Manipulando String em Python

A melhor maneira de manipular sequências de caracteres (Strings) em python é através de seus métodos. A seguir, apresentamos os principais métodos em Strings:
        ![string](/imagens/string.png)

``` python
subs = 'os'
texto='Como ser um bom programador? Simplesmente aprendendo a ler e interpretar textos\n aprender conceitos e não decorar comandos.\nPor fim, fazer muitos exercícios'

#conta quantas vezes aparece a string os no texto
conta = texto.count(subs)
print('quantidade de os = ', conta)
subs='amador'
#procura pela substring aramzenada em subs e retorna a posição inicial encontrada
posicao = texto.find(subs)
print('posição inicial da substring \"{0}\" no Texto = {1}'.format(subs,posicao))


texto1= ('Linguagem', 'de', 'programação', 'Python')
espaco = ' '
#Concatena o caracter espaço com entre as strings de texto1
texto2 = espaco.join(texto1)
print(texto2)

txt = "     Python     "
#Remove os caracteres (padrão espaços) do início e fim.as funções lstrip() e rstrip() removem a esquerda ou a direita somente 
x = txt.strip()

print("De todas as Linguagens", x, "é a minha favorita")

txt = ",,,,,Python....argh"

x = txt.strip(',.argh')
print("De todas as Linguagens", x, "é a minha favorita")

texto1 = 'A caixa 1 é azul, A caixa 2 é verde e caixa 3 é vermelha'
#Substitui a string caixa por lata em texto1
texto2 = texto1.replace('caixa', 'lata')
print(texto2)

```
