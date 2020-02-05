# Pacote MATPLOTLIB
O pacote **matplotlib** (http://matplotlib.org/) é uma biblioteca do Python utilizada para criação de gráficos em 2D, apresentando
uma série de possibilidades gráficas, como gráficos de barra, linha, pizza, histogramas, entre muitos outros.

### Importando o Pacote 
Para importar o pacote utilize a seguinte forma geral:
![funcao](/imagens/import_mat.png)

### Pyplot
O conjunto de funções disponível em **matplotlib.pyplot** permite a criação de uma figura e uma área padrão para exibir o gráfico na figura, necessitando apenas que você desenhe as linhas na área do gráfico, decore o gráfico com rótulos, etc. A seguir, um exemplo de código para gerar um gráfico simples:
``` python
import matplotlib.pyplot as plt
plt.plot( [1, 2, 3, 4, 5, 4, 3, 2, 1] )
plt.title("Simples Assim!!!")
plt.show()
```
![grafico](/imagens/grafico1.png)

O **plot()** é um método versátil, pois permite a definição de um número arbitrário de argumentos, como a cor da linha, o tipo de marca utilizada em cada ponto, tipo da linha, etc. Por exemplo, observe o exemplo a seguir:
``` python
medias = np.array([7.88, 5.21, 6.85, 5.90,  6.28, 8.46, 7.08, 3.41, 5.11, 8.11])

nomes = np.array(["Lucia","Ana", "Léo", "Bruno", "Michel", "Raul", "Lucas","Caio","Paulo", "Vitor"])

plt.plot(nomes, medias, 'bo')
plt.title('Médias x Alunos')
plt.show()
```
![grafico](/imagens/grafico2.png)

No exemplo acimma, o método **plot()** utiliza os arrays nomes (eixo x) e medias (eixo y) para plotar os pontos do gráfico. No comando, ainda existe um terceiro argumento opcional, que é a string de formatação indicando a cor e o tipo de linha do gráfico ('bo' - círculos azuis). 

As letras e os símbolos da sequência de formatação são do MATLAB. Pode-se concatenar uma sequência de cores com uma sequência de estilo de linha. A sequência de formato padrão é 'b-', que é uma linha azul sólida. No axemplo acima, utilizamos um gráfigo de pontos azuis. 

A seguir apresentamos as tabelas com os caracteres de formatação:
![grafico](/imagens/tabforma1.png)                       ![grafico](/imagens/tabforma2.png)                                                

Exemplo de gráfico com formatação:
``` python
#A função linspace cria uma seqüência de números (tam = 50), uniformemente espaçados, 
#entre os limites dados (0 e 1), opcionalmente incluindo o valor final 
x = np.linspace(0,1,num=50)

# Move os valores de x para y e os utiliza como os pontos do gráfico abaixo
y = x

#plotando a linha tracejada vermelha
plt.plot(x,y, linestyle = '--', color = 'r')  # ou 'r--'

# Move os quadrados de x para z e os utiliza como os pontos do gráfico abaixo
z = [t**2 for t in x]

#plotando a linha cheia azul
plt.plot(x,z, linestyle = '-', color = 'b') )  # ou 'b-'

# Move os cubos de x para z e os utiliza como os pontos do gráfico abaixo
w = [t**3 for t in x]

#plotando o tipo de marcador triângulo na côr verde
plt.plot(x,w, marker = '>', color = 'g')  

plt.show() 

```` 

![grafico](/imagens/grafico3.png)
