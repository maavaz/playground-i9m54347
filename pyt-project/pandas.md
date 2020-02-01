# Pacote Pandas

Semelhantemente ao pacote NumPy, o pacote **Pandas** está entre os mais utilizados no Python devido a sua utilidade para realizar análise de dados pelo seu desempenho e capacidade de simplificarem tarefas complicadas de manipulação de dados. O **Pandas** fornece estruturas de dados rápidas, flexíveis e expressivas, projetadas para facilitar o trabalho com dados estruturados (tabulares, multidimensionais, potencialmente heterogêneos) e de séries temporais.

Sendo assim, o primeiro passo para trabalhar com a biblioteca é importar o pacote. O formato geral é:

![funcao](/imagens/import_pandas.png)

### Pandas Series

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

O Pandas permite a aplicação de expressões matemáticas e funções matemáticas do numpy diretamente. No exemplo abaixo, a transformação da série contendo números pares (serie_par) para números ímpares (serie_impar) incrementado uma unidade a todos os elementos.

```python
In [16]: serie_impar = serie_par + 1
In [18]: serie_impar.head()
Out[18]: 
0    1
1    3
2    5
3    7
4    9
dtype: int32
```

Pode ser conveniente atribuirmos um índice diferente do padrão, supondo que essas sejam notas de uma turma, poderíamos atribuir nomes ao index: 
``` python
#Criando o array medias com as medias dos alunos (valores da Série)
In [5]: medias = np.array([7.88, 5.21, 6.85, 5.90,  6.28, 8.46, 7.08, 3.41, 5.11, 8.11])

#Criando o array nomes dos alunos que serão os índices da série
In [6]: nomes = np.array(["Luciano","Matheus", "Rodrigo", "Bruno", "Michel", "Raul", "Lucas","Caio","Paulo", "Vitor"])

#Criando a série turma com as médias e ps nomes como ídices
In [7]: turma = pd.Series(medias,index = nomes)

#Exibindo a coluna values (valores) da Série
In [11]: turma.values
Out[11]: array([7.88, 5.21, 6.85, 5.9 , 6.28, 8.46, 7.08, 3.41, 5.11, 8.11])

#Exibinddo a coluna index (índice) da Série
In [12]: turma.index
Out[12]: 
Index(['Luciano', 'Matheus', 'Rodrigo', 'Bruno', 'Michel', 'Raul', 'Lucas', 'Caio', 'Paulo', 'Vitor'],
      dtype='object')

#resultado mostra os nomes (índices) e as Médias (valores)
In [8]: turma.head()
Out[8]: 
Luciano    7.88
Matheus    5.21
Rodrigo    6.85
Bruno      5.90
Michel     6.28
dtype: float64

#Exibindo a média do aluno Paulo
turma['Paulo']
Out[9]: 5.11

#Exibindo a Média da Turma
print('Média da Turma: ', turma.mean())
Média da Turma:  6.428999999999999

#Exibido o Desvio Padrão
print('Desvio Padrão: ', turma.std())
Desvio Padrão:  1.574070801739518

#Exibindo um resumo Estatístico
In [12]: turma.describe()
Out[12]: 
count    10.000000
mean      6.429000
std       1.574071
min       3.410000
25%       5.382500
50%       6.565000
75%       7.680000
max       8.460000
dtype: float64

```

