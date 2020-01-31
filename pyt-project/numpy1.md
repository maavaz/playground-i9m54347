# Pacote NumPy

### Operações aritméticas com matrizes

**As operações aritméticas operam elemento a elemento:**

Os exemplos a seguir mostram  operações aritméticas com arrays. Caso deseje executá-los, utilize o editor ao final da página (copie e cole os comandos):

``` 
# importar o pacote NumPy
import numpy as np

# Criando o vetor a com 4 elementos
a = np.array([1, 2, 3, 4])
print('a = ',a)
# (Resultado) >>> a =  [1 2 3 4]

# criando o vetor b com os elementos de a incrementados de 1 unidade.
b = a + 1
print('b = ', b)
# (Resultado) >>> b =  [2 3 4 5]

# Criando o vetor b onde os elementos são potências de 2. Os elementos de a são os expoentes
b = 2**a
print('b = ', b)
# (Resultado) >>> b =  [ 2  4  8 16]

# Criando o vetor b com os elementos de a elevados ao quadrado
b = a ** 2
print('b = ', b)
# (Resultado) >>> b =  [ 1  4  9 16]

# Somando os elementos do vetor a
soma = a.sum() # ou sum(a)
print('soma = ', soma)
#(Resultado) >>> soma =  10

```

### Operações com matrizes (bi-dimensionais)

Os exemplos a seguir mostram  operações com matrizes bi-dimensionais. Caso deseje executá-los, utilize o editor ao final da página (copie e cole os comandos):
``` python
# importar o pacote NumPy
import numpy as np

# Criando as matrizes bi-dimensionais x e y
x = np.array([[1, 2], [1,2]])
y = np.array([[2,4], [3, 5]])

# Multiplicação dos elementos das matrizes x e y, criando uma nova matriz z com o resultado. 
# Isso não é multiplicação de matrizes
z = x * y
print('\nz =', z)
#(Resultado) >>>  z = [[2  8] [3 10]]

# Para realizar multiplicação das matrizes utilize a função dot().
# multiplicação das matrizes meu_array e divi_array
z = x.dot(y)
print('\nz =', z)
#(Resultado) >>> z = [[8 14] [8 14]]

# x * y é diferente y * x
z = y.dot(x)
print('\nz =', z)
#(Resultado) >>> z = [[6 12] [8 16]]

# Soma das Linhas e Colunas de uma matriz 3x3
x = np.array([[1, 1, 1], [2, 2, 2],[3, 3, 3]])

# Soma da colunas
z = x.sum(axis = 0)
print('z = ', z)
#(Resultado) >>> array([6, 6, 6])

#Soma das linhas
z = x.sum(axis = 1)
print('z = ', z)
#(Resultado) >>> array([3, 6, 9])

```
### Estatística utilizando matrizes  

Os exemplos a seguir mostram  operações com matrizes bi-dimensionais. Caso deseje executá-los, utilize o editor ao final da página (copie e cole os comandos):
``` python
# importar o pacote NumPy
import numpy as np
x = np.array([[1, 1, 1], [2, 2, 2],[3, 3, 3]])

# Criando uma matriz a partir de x com 2 linhas e 2 colunas
z = x[:2, :2]
print('\nz = ', z)
#(Resultado) >>> z = [[1 1] [2 2]]

# Criando uma mariz Transposta
a = np.array([[0, 1, 2], [3, 4, 5],  [6, 7, 8]])
b = a.T
print ('b = ', b)
#(resultado) >>> b =  [[0 3 6] [1 4 7] [2 5 8]]

# criando uma nova matriz com elementos maiores 2 a partir da matriz a
y = a[a>2]
print('y = ',y)
#(resultado) >>> y = [3  4  5  6  7  8]

# Rearrumando y para uma matriz 3 x 2
y = y.reshape(3, 2)
print('y = ', y)
#(Resultado) >>> y = [[3 4]  [5 6]  [7 8]]

#Encontra o menor valor da matriz x
minimo = x.min()
print('\nMínimo = ', minimo)
#(Resultado) >>> Mínimo =  1

#Encontra o maior valor da matriz x
maximo = x.max()
print('\nMáximo = ', maximo)
#(Resultado) >>> Máximo =  3

# Média dos elementos da Matriz
md = x.mean()
print('\nMédia = ', md)
#(Resultado) >>> Média =  2.0

# Variancia dos elementos da Matriz
vari = x.var()
print('\nVariância = ', vari)
#(Resultado) >>> Variância =  0.6666666666666666

# Desvio padrão dos elemntos da matriz
s = x.std() # = vari**0.5
print('\nDesvio Padrão = ', s)
#(Resultado) >>> Desvio Padrão =  0.816496580927726
```

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor2.sh" })

**ATENÇÃO: Como vocês puderam notar, o NumPy é realmente poderoso, pois pode executar grandes cálculos em uma única linha de código. Caso deseje tornar-se proficiente no NumPy, sugerimos ver a lista completa dos métodos ndarray na documentação do NumPy ndarray.**

