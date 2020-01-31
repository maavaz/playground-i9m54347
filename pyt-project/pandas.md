# Pacote Pandas

Semelhantemente ao pacote NumPy, o pacote **Pandas** está entre os mais utilizados no Python devido a sua utilidade para realizar análise de dados pelo seu desempenho e capacidade de simplificarem tarefas complicadas de manipulação de dados. O **Pandas** fornece estruturas de dados rápidas, flexíveis e expressivas, projetadas para facilitar o trabalho com dados estruturados (tabulares, multidimensionais, potencialmente heterogêneos) e de séries temporais.

Sendo assim, o primeiro passo para trabalhar com a biblioteca é importar o pacote. O formato geral é:

![funcao](/imagens/import_pandas.png)

###Panda Series

**Series** são matrizes unidimensionais rotuladas capazes de armazenar dados de qualquer tipo (inteiro, string, float, objetos python, etc.). Os rótulos dos eixos são chamados coletivamente de **índices**. Fazendo um paralelo com uma planilha MS-EXCEL uma série representa uma coluna em uma planilha do Excel.
Uma **Serie** suporta tanto a indexação inteira, quanto a baseada em rótulo e fornece uma série de métodos para executar operações envolvendo o índice.

A criação de uma série pode ser feita das seguintes formas:

+ A partir de um array - Uma série pode ser criada a partir de um array **NumPy**
``` python
In [1]: import numpy as np

In [2]: import pandas as pd

#Criando um numpy.array unidimensional com números pares de 0 a 1000 
In [3]: array_par = np.arange(0, 1001, 2, int)

# Criando a serie (serie_par) a partir do array (array_par)
In [4]: serie_par = pd.Series(array_par)

# Exibe as primeiras 5 linhas da série
In [5]: serie_par.head()  
Out[5]: 
0    0
1    2
2    4
3    6
4    8
dtype: int32
```
Como podemos notar no resultado apresentado acima, a série **serie_par** possui 2 colunas formadas pelos índices e os valores, os dois atributos fundamentais nesta estrutura. Como na criação da Serie não foi dado um índice específico o pandas usou os inteiros positivos crescentes como padrão. 

Pode ser conveniente atribuirmos um índice diferente do padrão, supondo que essas sejam notas de uma turma, poderíamos atribuir nomes ao index: 


