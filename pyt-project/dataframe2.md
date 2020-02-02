# Pacote Pandas

### Criando DataFrame (Continuação)

+ Criando DataFrame a partir da leitura dos dados de um arquivo (p.ex. csv). 

O arquivo que será utilizado nesse exemplo tem sua fonte (alterado):  Countries of the World (http://gsociology.icaap.org/dataupload.html)

![funcao](/imagens/paises.png)

```python
#Importando as bibliotecas 
In [1]: import numpy as np

In [2]: import pandas as pd

#Criando um DataFrame a partir do Arquivo .csv. As colunas do arquivo não serão usadas como índice (index_col=False)
In [3]: df = pd.read_csv('paisesdomundo.csv', index_col=False)

#Exibindo os Nomes e população dos países com menos de cem  mil habitantes  
In [8]: df.loc[df['População'] <= 100000, ['País','População']]
Out[8]: 
                      País  População
6      Antigua and Barbuda      69108
48                Dominica      68910
67                 Granada      89703
80          Ilhas Marshall      60422
119                  Nauru      13287
127                  Palau      20579
151  São Cristóvão e Nevis      39129
152             São Marino      29251
158             Seychelles      81541
178                 Tuvalu      11810

#Exibindo apenas as colunas País (coluna 0), Região (coluna 1) e População (coluna 2) do País com índice 24
In [10]: df.iloc[24][0:3]
Out[10]: 
País                           Brasil
Região       AMÉRICA  LATINA & CARIBE
População                   188078227
Name: 24, dtype: object

#Exibindo os nomes dos 7 primeiros países
In [11]: df['País'].head(7)
Out[11]: 
0            Afeganistão
1          África do Sul
2                Albania
3               Alemanha
4                Algeria
5                 Angola
6    Antigua and Barbuda
Name: País, dtype: object
```
