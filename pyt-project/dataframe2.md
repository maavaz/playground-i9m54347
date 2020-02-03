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
### Seleção de dados do Pandas
Existem várias maneiras de selecionar e indexar linhas e colunas dos DataFrames do Pandas, mas existem 3 possíveis maneiras para realizar as atividades de seleção e indexação no Pandas que são:
+ Selecionando os dados pela técnica de Slice
+ Selecionando dados por números de linha (.iloc)
+ Selecionando dados por rótulo ou por uma declaração condicional (.loc)

``` python
#Criando um DataFrame a partir do Arquivo .csv. As colunas do arquivo não serão usadas como índice (index_col=False)
In [1]: df = pd.read_csv('paisesdomundo.csv', index_col=False)

#Selecionando o dois primeiros registros
In [2]: df[:2]
Out[2]: 
            País              Região  População   área (milhas quadradas)  \
0    Afeganistão    SUDOESTE DA ÁSIA   31056997                    647500   
1  África do Sul  ÁFRICA SUBSAARIANA   44187637                   1219912   

                               Descrição     Unidade   Escala      2015  \
0  Produto interno bruto - preços atuais  US dollars  Bilhões   19687.0   
1  Produto interno bruto - preços atuais  US dollars  Bilhões  314732.0   

       2016      2017      2018      2019      2020      2021      2022  
0   18886.0   20570.0   21706.0   23233.0   24930.0   26857.0   29113.0  
1  294132.0  317568.0  326967.0  339846.0  353409.0  366860.0  380425.0  

#Selecionando o nome dos países dos 3 primeiros registros 
In [3]: df[:3]['País']
Out[3]: 
0      Afeganistão
1    África do Sul
2          Albania
Name: País, dtype: object

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

#Exibindo a média dos PIB de 2017 (7) a 2022 (11) do País de índice 24 (Brasil)
In[13] : df.iloc[24][7:].mean()
Out[13]: 2009638.375

#Exibindo o Nome do País com população superior a Um bilhão e trezentos milhões de habitante. Utilizando uma função lambda
In [14]: print(df.loc[lambda df: df['População']>1300000000]['País'])
37    China
Name: País, dtype: object

#repetindo o exemplo anterior sem o uso da função lambda.
In [15]: df.loc[df['População']>1300000000, ['País']]
Out[15]: 
     País
37  China

```
