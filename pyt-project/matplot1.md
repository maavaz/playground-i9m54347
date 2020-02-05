# Pacote MatPlotLib

### Tipos de Gráficos
Apresentamos alguns tipos de graficos mais comuns.

### Gráfico de Barras
Para esse tipo de gráfico existe a função **bar()** que permite a definição de algumas características, como a espessura das barras, côr, entre outros. O eixo X deve ter a mesma quantidade de itens do eixo Y.  
``` phyton
valor = np.array([20,22,24,26,28,30,32])	
freq = np.array([100, 150, 170,180, 160, 120, 90])

width_n = 1.75   # Largura das Colunas 
bar_color = 'k'  # Côr da barra = Preto

plt.bar(valor, freq, width=width_n, color=bar_color)
plt.show()
```
![grafico](/imagens/graf_bar.png)

### Gráfico Pie Chart
O gráfico Pie Chart (pizza) é um diagrama circular onde os valores de cada categoria são representados proporcionais às respectivas frequências. Este gráfico pode vir acompanhado de porcentagens. Para construir um gráfico tipo pizza é necessário determinar o ângulo dos setores circulares (startangle) correspondentes à contribuição percentual de cada valor no total. O exemplo a ser exibido corresponde a tabela abaixo:

![funcao](/imagens/candidatos.png)
``` python
import matplotlib.pyplot as plt
import numpy as np
votos = np.array([842.201, 488.775, 553.424, 424.307, 272.500, 381.512, 261.386])
candi = ['Candidato A', 'Candidato B', 'Candidato C', 'Candidato D', 'Candidato E',
         'Candidato F', 'Candidato G']

cores=['gold', 'red', 'blue', 'magenta', 'green','lightskyblue', 'yellowgreen']
# o atributo explode indica que fatia do gráfico será destacada. No exemplo abaixo, será a primeira fatia. A quantidade de valores é igual ao número de fatias do gráfico. 
explode = (0.1, 0, 0, 0, 0, 0, 0)  # explode 1st slice

# Atribuindo um título ao gráfico
plt.title('Eleição 2020 - Total de Votos')

plt.pie(votos, explode=explode, labels=candi, colors=cores, autopct='%1.1f%%', shadow=True, startangle=90)

#Adiociona Legenda
plt.legend(candi, bbox_to_anchor=(1.3, 1.3),loc='upper right')

#Centraliza o gráfico
plt.axis('equal')

#Ajusta o espaçamento para evitar o recorte do rótulo
plt.tight_layout()

plt.show()

```
![funcao](/imagens/piechart.png)

### Gráfico Histograma
Um histograma é um gráfico de frequência que tem como objetivo ilustrar como uma determinada amostra ou população de dados está distribuída.
A amostra de dados é dividida em intervalos (classes) onde são computadas e distribídas as frequências. 

Para se achar o número correto de intervalos (bis) devemos considerar as informações abaixo:
tamanho = número de itens da amostra
Range = valor máximo - valor mínimo da amostra
número de intervalos =  Raiz quadrada de tamanho
largura de cada intervalo =  Range / número de intervalos


``` phyton
idade= ([19, 21, 23, 25, 25, 29, 31, 33, 35, 37, 39, 41, 31, 19,
         40, 34, 28, 32, 29, 34, 27, 27, 36, 29, 37, 31, 29, 33, 
         34, 39, 26, 27, 37, 33, 38, 34, 33, 29, 36, 28, 27, 34,
         28, 27, 30, 28, 37, 37, 32, 36, 34, 38, 29, 30, 20, 30,
         31, 25, 32, 27, 28, 38, 29, 28, 33, 37, 40, 41, 40, 27,
         30, 27, 25, 25, 29, 25, 39, 29, 39, 24, 25, 28, 24, 29, 
         29, 24, 24, 28, 31, 36, 24, 24, 33, 34, 31, 28, 24, 30,
         31, 37, 17, 30, 27, 32, 35, 26, 26, 34, 33, 25, 24, 32,
         32, 22, 30, 25, 32, 25, 21, 20, 30, 29, 18, 23, 23, 35, 
         20, 18, 27, 29, 17, 35, 17, 21, 28, 17, 23, 25, 24, 23,  
         20, 29, 22, 21, 22, 26, 19, 24, 25, 22, 19, 23, 18, 22, 
         35, 30, 28, 27, 29, 29, 22, 25, 22, 29, 26, 22, 19, 22, 
         33, 24, 29, 28, 19, 26, 29, 19, 31, 21, 21, 26, 31, 29])

#Tamanho da amostra
tamanho= len(idade)

# quantidade de Classes (bins)
cl = int(round(tamanho**(1/2),0))

# estilo ggplot (vermelho)
plt.style.use('ggplot')

plt.hist(idade, bins = cl, density=1)

plt.tight_layout()
plt.show()


```

**OBS:** Apresentamos apenas alguns tipos de gráficos, mas há uma grande variedade de exemmplos, inclusive com código fonte, de gráficos no endereço: https://matplotlib.org/api/_as_gen/matplotlib.pyplot.subplot.html.
