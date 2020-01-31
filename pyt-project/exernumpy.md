``` python
import numpy as np

arr = np.array([4, 5, 6, 7, 8, 10, 12])

arr = arr**2

print (arr[4])
```
?[Qual o resultado da execução do trecho de código acima?](single)
-[ ] 25
-[ ] 49 
-[x] 64
-[ ] 100

``` python
import numpy as np

a = np.array([1,3,5,7])
b = np.array([0,2,4,6])
c = a + b
print (c)
```
?[Qual o resultado da execução do trecho de código acima?](single)
-[ ] [28]
-[ ] [0, 1, 2, 3, 4, 5, 6, 7] 
-[ ] [1, 3, 5, 7, 0, 2, 4, 6]
-[x] [1, 5, 9, 13]

``` python
a = np.zeros((2,3), dtype=int)
b = np.ones((2,3), dtype=int)
c = a + b
print (c[1,2])
```
?[Qual o resultado da execução do trecho de código acima?](single)
-[ ] 0
-[x] 1 
-[ ] 2
-[ ] 3
