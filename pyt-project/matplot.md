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

O **plot** é um método versátil, pois permite a definição de um número arbitrário de argumentos, como a cor da linha, o tipo de marca utilizada em cada ponto, tipo da linha, etc. Por exemplo, observe o exemplo a seguir.
