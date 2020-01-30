# Pacote NumPy

NumPay é uma poderosa biblioteca, cuja estrutura de dados principal é a matriz multidimensional, chamada ndarray. Na programação, matriz representa uma coleção de elementos de mesmo tipo, semelhante a uma lista. A palavra multidimensional ou n-dimensional refere-se ao fato de que as matrizes podem ter uma ou mais dimensões. 
Para podermos utilizar as funções da biblioteca devemos utilizar o comando **import**, conforme figura abaixo:

![funcao](/imagens/import_numpy.png)

Iniciaremos com utilizando exemplos com arrays unidimensionais ou vetores:
![funcao](/imagens/vetor.png)

+ A individualização de cada elemento do vetor é feita através do uso de índices. O acesso ao conteúdo de um determinado item é semelhante as listas, isto é, nome da variável array seguido de colchetes e o número do índice que se deseja acessar.
``` python
nome_da_variável_array[indice]
```
+ Os vetores tem o primeiro elemento na posição **0 (zero)**. Assim, se tomarmos **"K"** como sendo o tamanho do vetor a última posição é a de índice **"K-1"**. Por exemplo, um vetor de tamanho 10 (k=10) tem o seu último elemento na posição 9.

+ O vetor por ser unidimensional precisa de apenas 1 índice para acesso aos elementos, enquanto que as matrizes n-dimensionais, necessitam de um índice para cada dimensão para acesso aos itens da matriz.

![funcao](/imagens/array.png)

Os exemplos a seguir mostram  a criação de um array unidimensional, bem como algumas funções úteis com arrays. Caso desejar executá-los, utilize o editor ao final da página (copie e cole os comandos):

``` python
# importar o pacote NumPy
import numpy as np

# Criando um vetor contendo 10 elementos
meu_array = np.array([10, 20, 30, 40, 50, 60, 70, 80, 90, 100])
print('meu_array=', meu_array)
# (Resultado) >>> meu_array= [ 10  20  30  40  50  60  70  80  90 100]

# Exibindo a quantidade de elementos do vetor
print('Tamanho do vetor = ', meu_array.size)
# (Resultado) >>> Tamanho do vetor =  10

# Exibindo o conteúdo do item na quinta posição do vetor
print('quinto elemento: ', meu_array[4])
# (Resultado) >>> quinto elemento:  50

# Dividindo todos os itens do vetor por 10 e criando um novo vetor (tipo float)
divi_array = meu_array / 100
print ('divi_array = ', divi_array)
# (Resultado) >>> divi_array =  [0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 1. ]

# Cria o vetor novo_array com 5 elementos inicializado com zeros.
novo_array = np.zeros(5)
print('novo_arrray = ', novo_array)
# (Resultado) >>> novo_arrray =  [0. 0. 0. 0. 0.]

# Cria o vetor novo_array com 5 elementos inicializado com 1 (float).
novo_array = np.ones(5)
print('novo_arrray = ', novo_array)
# (Resultado) >>> novo_arrray =  [1. 1. 1. 1. 1.]

# Cria o vetor novo_array com 5 elementos inicializado com 1 (intt).
novo_array = np.ones((5), dtype=int)
print('novo_arrray = ', novo_array)
# (Resultado) >>> novo_arrray =  [1 1 1 1 1]

```
**As operações aritméticas operam elemento a elemento:**

Os exemplos a seguir mostram  operações aritméticas com arrays:

``` python runnable
# importar o pacote NumPy
import numpy as np

# Criando o vetor a com 4 elementos
a = np.array([1, 2, 3, 4])
print('a = ',a)
# criando o vetor b com os elementos de a incrementados de 1 unidade.
b = a + 1
print('b = ', b)

# Criando o vetor b onde os elementos são potências de 2. Os elementos de a são os expoentes
b = 2**a
print('b = ', b)

# Criando o vetor b com os elementos de a elevados ao quadrado
b = a ** 2
print('b = ', b)
```
O editor abaixo contem os exemplos exibidos acima:

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor1.sh" })
