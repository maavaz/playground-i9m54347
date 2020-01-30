# Pacote NumPy

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

```

**Operações com matrizes (bi-dimensionais):**

Os exemplos a seguir mostram  operações com matrizes bi-dimensionais. Caso deseje executá-los, utilize o editor ao final da página (copie e cole os comandos):
