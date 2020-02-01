# Pacote Pandas

+ A partir de um arquivo - Iremos carregar os dados (colunas) Nomes dos jogadores (índice) e idade que possui (valores) de uma planilha MS_EXCEL, exibida em parte, abaixo:
![funcao](/imagens/excel.png)

``` python
#Importando a bibliotecas
In [1]: import numpy as np

In [2]: import pandas as pd

In [3]: dado = pd.read_excel('C:/Python36-32/CariocaFutebol.xlsx')

In [4]: idade = np.array(dado['Idade']).astype(int)

In [5]: jogadores = pd.Series(idade, index=dado['Nome'])

In [6]: jogadores.tail()
Out[6]: 
Nome
Douglas Lima         25
João Vitor           22
Pedrinho Henrique    23
Saulo Mineiro        22
Andrey Jacaré        16
dtype: int32

In [7]: jogadores['Raul']
Out[7]: 23

```
