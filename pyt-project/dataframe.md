# Pacote Pandas

### Pandas DataFrame

Pandas DataFrame é uma estrutura de dados bidimensional com os dados alinhados de forma tabular em linhas e colunas, mutável em tamanho e potencialmente heterogênea, semelhantemente a uma planilha MS-EXCEL.  

![funcao](/imagens/tabFrame.png)

## Criando um DataFrame

Em geral, o DataFrame pode conter dados a partir de:
+ Um DataFrame do Pandas
``` python
#Importando a biblioteca Pandas
In [1]: import pandas as pd

#Criando um Dataframe com 2 linhas (indexes 0 e 1) e 4 colunas ('Idade', 'Sexo', 'Peso', 'Altura').
In [2]: meu_df = pd.DataFrame([[21,'F', 50, 1.57],[22,'F',58, 1.70]], index=range(0,2), columns=['Idade', 'Sexo', 'Peso', 'Altura'])

#Exibindo o DataFrame criado
In [3]: meu_df
Out[3]: 
   Idade Sexo  Peso  Altura
0     21    F    50    1.57
1     22    F    58    1.70

#Acesso as linhas do DataFrame a partir do seu índice. Utilizar a função .iloc[indice].
#Exibir a segunda linha do Dataframe
In [4]: meu_df.iloc[1]
Out[4]: 
Idade      22
Sexo        F
Peso       58
Altura    1.7
Name: 1, dtype: object
```
+ Uma Série Pandas: um array unidimensional capaz de armazenar qualquer tipo de dados com rótulos ou índice de eixo. Um exemplo de um objeto Series é uma coluna de um DataFrame.
``` phyton
#Criando uma Série formada por nomes e com índices de 0 até 4.
In [4]: nomes = pd.Series(["Luciano","Matheus", "Rodrigo", "Bruno", "Michel"], index=range(0,5))

#Criando um DataFrame a partir da Serie nomes com a coluna denominada Nomes    
In [5]: df = pd.DataFrame(data=nomes, columns=['Nomes'])

In [6]: df
Out[6]: 
     Nomes
0  Luciano
1  Matheus
2  Rodrigo
3    Bruno
4   Michel

```
