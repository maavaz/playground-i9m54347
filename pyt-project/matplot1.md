# Pacote MatPlotLib

### Tipos de Gráficos
Apresentamos alguns tipos de graficos mais comuns.

### Gráficos de Barras
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

### Grafico Pie Chart
O gráfico Pie Chart (pizza) é um diagrama circular onde os valores de cada categoria são representados proporcionais às respectivas frequências. Este gráfico pode vir acompanhado de porcentagens. Para construir um gráfico tipo pizza é necessário determinar o ângulo dos setores circulares (startangle) correspondentes à contribuição percentual de cada valor no total. O exemplo a ser exibido corresponde a tabela abaixo:

![funcao](/imagens/candidatos.png)
``` python


```




![funcao](/imagens/piechart.png)
