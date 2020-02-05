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

**OBS:** Apresentamos apenas alguns tipos de gráficos, mas há uma grande variedade de exemmplos, inclusive com código fonte, de gráficos no endereço: https://matplotlib.org/api/_as_gen/matplotlib.pyplot.subplot.html.
