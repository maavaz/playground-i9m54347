# Pacote Pandas

+ A partir de um arquivo - Iremos carregar os dados (colunas) Nomes dos jogadores (índice) e idade que possui (valores) de uma planilha MS_EXCEL, exibida em parte, abaixo:
![funcao](/imagens/excel.png)

``` python
#Importando as bibliotecas
In [1]: import numpy as np

In [2]: import pandas as pd

#Efetuando a Leitura dos dados da Planilha MS-EXCEL 'CariocaFutebol.xls'
In [3]: dado = pd.read_excel('C:/Python36-32/CariocaFutebol.xlsx')

#Criando o array idade transformados para o tipo int (os campos numéricos da planilha são carregado como float)
In [4]: idade = np.array(dado['Idade']).astype(int)

#Criando a série jogadores com o campo de valores idades e campo índices nomes
In [5]: jogadores = pd.Series(idade, index=dado['Nome'])

#Exibindo os últimos 5 elementos da Série
In [6]: jogadores.tail()
Out[6]: 
Nome
Douglas Lima         25
João Vitor           22
Pedrinho Henrique    23
Saulo Mineiro        22
Andrey Jacaré        16
dtype: int32

#Exibindo a idade do jogador 'Raul'
In [7]: jogadores['Raul']
Out[7]: 23

#Exibindo a idade do jogador de índice 10 (Léo Amorim)
In [8]: jogadores[10]
Out[8]: 19

```
