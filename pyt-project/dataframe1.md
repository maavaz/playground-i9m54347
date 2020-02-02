# Pacote Pandas

+ uma matriz bidimensional, que pode ser um registro ou estruturada
``` phyton
#Importando a bilbioteca Pandas
In [1]: import pandas as pd

#Criando o numpy.array (data) bidimensional (3X3)
In [2]: data =np.array([['Portugal', 'Lisboa', 10000000],
   ...:                 ['Peru', 'Lima', 32000000],
   ...:                 ['Chile', 'Santiago', 18000000],
   ...:                 ['Brasil', 'Brasília', 209000000]])

#Criando o DataFrame com o np.array (data) com as colunas ('País', 'Capital', 'População'), indexado de 100 até 103
In [3]: df = pd.DataFrame(data, index=range(100,104),columns=['País', 'Capital', 'População'])

#Exibindo o DataFrame
In [4]: df
Out[4]: 
         País   Capital  População
100  Portugal    Lisboa   10000000
101      Peru      Lima   32000000
102     Chile  Santiago   18000000
103    Brasil  Brasília  209000000

#Exibindo uma linha do DataFrame selecionando a partir do índice. Para isso, utilizamos a função .loc[indice]
In [5]: df.loc[102]
Out[5]: 
País            Chile
Capital      Santiago
População    18000000
Name: 102, dtype: object

```
+ um ndarray bidimensional
+ dicionários de ndarray unidimensionais, listas, dicionários ou Séries.
