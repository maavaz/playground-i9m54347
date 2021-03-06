# Pacote NumPy

<b>NumPay</b> é uma poderosa biblioteca, cuja estrutura de dados principal é a matriz multidimensional, chamada ndarray. Na programação, matriz representa uma coleção de elementos de mesmo tipo, semelhante a uma lista. A palavra multidimensional ou n-dimensional refere-se ao fato de que as matrizes podem ter uma ou mais dimensões. 
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

+ A técnica de **slice** para selecionar subconjuntos de dados de uma matriz, pode ser utilizada em NumPY 

Os exemplos a seguir mostram  a criação de um array unidimensional, bem como algumas funções úteis com arrays. Caso deseje executá-los, utilize o editor ao final da página (copie e cole os comandos):

``` python
# importar o pacote NumPy
import numpy as np

# Criando um vetor contendo 10 elementos
meu_array = np.array([10, 20, 30, 40, 50, 60, 70, 80, 90, 100])
print('meu_array=', meu_array)
# (Resultado) >>> meu_array= [ 10  20  30  40  50  60  70  80  90 100]

# Exibindo a quantidade de elementos do vetor
print('\nTamanho do vetor = ', meu_array.size)
# (Resultado) >>> Tamanho do vetor =  10

# Exibindo o conteúdo do item na quinta posição do vetor
print('\nquinto elemento: ', meu_array[4])
# (Resultado) >>> quinto elemento:  50

# Criando um novo array com elementos de x com índices de 3 até 8
s = meu_array[3:8]
print('\ns = ', s)
# (Resultado) >>> s =  [40 50 60 70 80]

# Dividindo todos os itens do vetor por 10 e criando um novo vetor (tipo float)
divi_array = meu_array / 100
print ('\ndivi_array = ', divi_array)
# (Resultado) >>> divi_array =  [0.1 0.2 0.3 0.4 0.5 0.6 0.7 0.8 0.9 1. ]

# Cria o vetor novo_array com 5 elementos inicializado com zeros.
novo_array = np.zeros(5)
print('\nnovo_arrray = ', novo_array)
# (Resultado) >>> novo_arrray =  [0. 0. 0. 0. 0.]

# Cria o vetor novo_array com 5 elementos inicializado com 1 (float).
novo_array = np.ones(5)
print('\nnovo_arrray = ', novo_array)
# (Resultado) >>> novo_arrray =  [1. 1. 1. 1. 1.]

# Cria uma matriz 2x2 (novo_array) inicializada com 1 (int).
novo_array = np.ones((2,2), dtype=int)
print('\nnovo_arrray = ', novo_array)
# (Resultado) >>> novo_arrray =  [[1 1]  [1 1]]

# Cria um vetor com valores uniformemente distribuídos dentro de um intervalo especificado.
novo = np.arange(1, 10, 1, int) # Vetor com 9 elementos iniciando em 1 até 9 (limite superior não incluso), incrementado de 1 unidade
print('\nnovo = ', novo)
# (Resultado) >>> novo = [1  2  3  4  5  6  7  8  9]

```

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor1.sh" })
