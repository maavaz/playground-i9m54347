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

#Exibindo os dados de uma coluna (Capital), usada como índice do DataFrame
In [6]: df['Capital']
Out[6]: 
100      Lisboa
101        Lima
102    Santiago
103    Brasília
Name: Capital, dtype: object

#Exibindo as linhas onde a População é maior que 10 milhões de habitantes. Utilizamos a função .loc[condicional]
In [23]: df.loc[df['População'] > '10000000']
Out[23]: 
       País   Capital  População
101    Peru      Lima   32000000
102   Chile  Santiago   18000000
103  Brasil  Brasília  209000000


```
+ Um ndarray bidimensional

``` python
#Criando o array bidimensional 2x3
In [8]: x = np.array([[1, 2, 3], [4, 5, 6]], np.int32)

#Criando o DataFrame a partir do ndarray 2x3, renomeando as colunas
In [9]: df=pd.DataFrame(x, columns=['col1', 'col2', 'col3'])

In [10]: df
Out[10]: 
   col1  col2  col3
0     1     2     3
1     4     5     6

```

+ Dicionários de ndarray unidimensionais, listas, dicionários ou Séries.

``` phyton


```
