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

Os exemplos a seguir mostram  a criação de um array unidimensional, bem como algumas funções úteis com arrays:

``` python
# importar o pacote NumPy
import numpy as np

# Criando um vetor contendo 10 elementos
meu_array = np.array([10, 20, 30, 40, 50, 60, 70, 80, 90, 100])

# Exibindo a quantidade de elementos do vetor
print('Tamanho do vetor = ', meu_array.size)

# Exibindo o conteúdo do item na quinta posição do vetor
print('quinto elemento: ', meu_array[4])

# Cria o vetor novo_array com 5 elementos inicializado com zeros.
novo_array = np.zeros(5)
print(novo_array)

# Cria o vetor novo_array com 5 elementos inicializado com 1 (float).
novo_array = np.ones(5)
print(novo_array)

# Cria o vetor novo_array com 5 elementos inicializado com 1 (intt).
novo_array = np.ones((5), dtype=int)
print(novo_array)
```
O editor abaixo contem os exemplos exibidos acima:

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor1.sh" })

**Todas as operações aritméticas operam elemento a elemento:**
``` python runnable
# importar o pacote NumPy
import numpy as np

# Criando um vetor contendo 10 elementos
meu_array = np.array([1, 2, 3, 4])

# Exibir os elementos do array incrementados de 1 unidade
print(meu_array + 1)

# Exibir o resultado da potenciação de 2 por cada elemento do vetor
print(2**meu_array)

# Exibir os elementos do vetor elevado ao quadrado
print(meu_array**2)
```
O editor abaixo contem os exemplos exibidos acima:

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor1.sh" })

Multiplicação de array não é multiplicação de matrizes, para realizarmos a multiplicação das matrizes deveos usar a função **dot()**
