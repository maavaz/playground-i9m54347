# Exercitando

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
-[ ] [0  1  2  3  4  5  6  7] 
-[ ] [1, 3  5  7  0  2  4  6]
-[x] [1  5  9  13]

``` python
a = np.zeros((2,3), dtype=int)
b = np.ones((2,3), dtype=int)
c = a + b
print (c[1,2])
```
?[Qual o resultado da execução do trecho de código acima?](single)
-[ ] 0
-[x] 1 
-[ ] 4
-[ ] 6

``` python
import numpy as np

a = np.array([[0, 1, 2], [3, 4, 5]])
b = a.sum(axis=1)
print (b)

```
?[Qual o resultado da execução do trecho de código acima?](single)
-[ ] [3 5 7]
-[x] [3 12]
-[ ] [12]
-[ ] Erro!!!

### <b> Exercício 1 </b>

Faça um programa que, a partir das matrizes de notas e pesos apresentadas abaixo, calcule as médias da notas (arredondadas com 2 casas decimais), considerando os pesos de cada uma (média ponderada). Exiba:
+ média de cada aluno;
+ média geral da turma;
+ quantidade de médias acima da média geral;
+ menor média da turma;
+ maior média da turma.
``` python
notas = np.array([[9.28,0.93,3.92,8.98,3.7],[9.1,5.04,3.68,0.22,8.86],[6.83,3.79,9.39,2.59,7.12],
                  [8.92,1.72,7.85,1.08,5.27], [8.25,4.56,4.54,9.13,9.88],[4.39,5.48,3.26,8.08,3.78],
                  [6.32,4.09,9.45,4.8,7.39],[4.51, 0.61,2.74,4.25,8.67], [5.1,9.4,4.05,5.42,0.51],
                  [0.45,2.18,7.47,6.44,1.76],[2.35,5.73,1.59,2.07,0.82],[1.53,6.04,5.98,3.97,5.53],
                  [5.8,7.68,1.53,7.28,1.32],[3.93,7.79,8.56,1.09,3.78],[8.42,1.53,8.53,9.88,3],
                  [0.88,0.39,8.23,8.1,7.57],[2.7,3.72,4.29,9.66,1.68],[4.97,7.83,6.53,1.89,8.22],
                  [7.94,4.97,6.54,2.6,3.93],[4.9,7.44,4.31,9.57,9.86],[1.09,4.73,4.81,2.92,4.72],
                  [7.61,3.52,6.4,9.98,8.27],[9.19,4.38,3,5.9,8.81],[0.92,0.92,0.67,4.88,6.66],
                  [6.39,1.85,2,6.91,4.13],[3.65,0.41,2.95,6.05,7.91],[6.29,7.34,1.34,3.02,8.8],
                  [6.25,4.2,3.25,6.14,6.21],[9.2,9.73,5.42,5.5,1.92],[0.1,6.77,1.85,7.6,0.21],
                  [4.37,4.29,9.42,9,0.73],[5.1,9.38,8.84,3.92,9.4],[10,5.54,7.37,6.74,10],
                  [5.35,4.83,6.8,6.98,7.08],[8.03,6.59,7.44,7.38,4.74],[7.88,8.21,6.17,6.07,9.11],
                  [3.88,5.93,6.87,4.25,2.61],[5.41,5.13,5.83,7.85,4.09],[4.48,9.1,2.84,6.65,3.08],
                  [5.04,2.03,6.73,4.7,3.56],[5.32,7.37,8.01,8.23,2.2],[6.82,9.31,7.44,3.08,3.65],
                  [1.26,6.3,6.44,7.69,7.07],[7.9,8.75,2.47,2.69,4.43],[4.33,7.45,8.04,2.88,9.06],
                  [2.38, 1.21, 5.12, 1.25, 3.86],[5.39, 1.62, 2.14, 7.41, 1.79],[4.72,2.52,7.76,4.47,6.07],
                  [8.59,4.52,3.07,5.42,3.36],[5.42,7.35,5.26,3.95,1.95],[4.92, 9.76, 1.3, 0.6, 4.45],
                  [5.37, 9.76, 8.55, 6.65, 9.99],[6.52, 5.43, 3.28, 8.59, 8.75],[5.52, 7.29, 2.04, 1.84, 7.39],
                  [8.85, 3.07, 3.66, 8.76, 6.22],[9.63, 8.75, 2.43, 2.65, 05.61],[8.34, 7.36, 1.31, 9.31, 1.03],
                  [2.1, 8.42, 1.32, 1.17, 9.97],[9.97, 4, 3.01, 4.26, 1.16],[2.2, 2.64, 8.94, 9.57, 7.67],
                  [6.57, 9.05, 4.75, 6.81, 9.11],[8.3, 2.52, 4.47, 4.82, 6.67],[7.09, 5.35, 3.99, 0.25, 8.04],
                  [6.84, 7.81, 6, 5.69, 8.57],[3.52, 3.64, 7.31, 9.84, 6.04],[8.89, 6.68, 1.99, 3.02, 9.83],
                  [1.26, 8.25, 1.9, 6.32, 6.84],[7.54, 2.07, 2.18, 9.84, 1.93],[2.84, 2.76, 1.84, 3.52, 9.3],
                  [9.04, 3.23, 1.02, 7.71, 7.75],[4.7, 7.15, 8.36, 2.36, 4.88],[5.76, 5.24, 4.57, 7.11, 0.41],
                  [1.36, 1.12, 2.65, 1.86, 7.96],[3.31, 9.42, 4.46, 4.28, 2.86],[6.55, 6.81, 4.87, 9.26, 6.82],
                  [1.33, 5.69, 5.36, 4.96, 8.33],[9.76, 9.17, 4.96, 9.61, 7.03],[7.62, 2.75, 8.35, 4.79, 3.87],
                  [2.82, 3.51, 1.8, 4.81, 8.25],[2.37, 7.19, 6.77, 8.49, 7.77],[4.72, 6.75, 7.67, 2.94, 1.81],
                  [4.03, 5.03, 1.83, 9.69, 7.67],[2.91, 6.97, 9.1, 4.69, 4.9],[8.97, 3.95, 5.77, 8.67, 9.38],
                  [1.7, 5.42, 8.12, 2.79, 8.95],[6.83, 7.74, 9.27, 4.96, 4.92],[2.16, 5.37, 5.38, 9.61, 8.86],
                  [1.28, 4.85, 6.64, 7.36, 2.44],[7.37, 6.19, 9.81, 7.8, 4.83],[7.84, 9.07, 8.11, 7.72, 8.49],
                  [5.48, 9.19, 8.22, 4.77, 8.14],[4, 2.63, 3.67, 4.57, 7.56],[0.6, 8.45, 2.26, 1.69, 1.6],
                  [6.89, 5.84, 6.47, 5.27, 7.27],[6.33, 3.74, 5.85, 8.33, 8.93],[8.38, 3.19, 5.78, 8.99, 7.69],
                  [3.81, 5.33, 6.67, 8.69, 7.33],[6.73, 8.34, 6.07, 1.88, 8.3],[8.88, 1.45, 3.72, 3.93, 6.85],
                  [2.43, 2, 4.21, 5.96, 7.89],[9.82, 6.86, 7.52, 4.59, 5.39],[4.55, 3.91, 0.7, 7.43, 7.97],
                  [0.64, 9.47, 6.67, 2.46, 4.54],[4.57, 9.52, 3.22, 3.26, 3.59],[4.08, 0.46, 4.4, 4.17, 0.27],
                  [4.8, 7.73, 8.06, 3.98, 4.79],[3.03, 2.7, 1.78, 6.31, 8.49],[4.18, 1.71, 7.74, 5.61, 0.72],
                  [5.33, 3.37, 7.89, 2.41, 1.93],[7.49, 7.92, 5.98, 7.94, 8.9],[4.62, 7.83, 7.3, 3.09, 8.46],
                  [2.07, 6.82, 9.32, 3.42, 6.29],[4.73, 9.98, 3.1, 6.39, 8.57],[5.13, 2.22, 9.39, 6.4, 4.66],
                  [7.88, 9, 3.56, 2.62, 4.76],[1.91, 9.09, 5.56, 2.39, 8.86],[8.84, 1.72, 6.87, 6.4, 7.95],
                  [8.53,2.56, 4.45, 7.64, 5.57],[4.44, 3.69, 4.79, 9.17, 6.03],[9.75, 6.7, 7.56, 7.12, 8.88],
                  [5.23, 5.59, 7.62, 9.75, 9.26],[1.02, 8.2, 9.41, 1.92, 2.46],[3.27, 3.42, 1.33, 6.37, 7.47],
                  [2.31, 5.31, 5.9, 4.47, 7.47],[1.46, 6.75, 4.87, 7.66, 8.84],[5.82, 9.27, 6.84, 2.5, 4.39],
                  [9.99, 1.26, 6.96, 1.03, 8.72],[1.46, 4.33, 1.41, 5.78, 4.67],[5.88, 5.98, 9.34, 6.75, 2.6],
                  [9.82, 8.39, 8.36, 2.4, 3.63],[2.76, 3.64, 9.24, 1.91, 6.49],[1.55, 8.71, 4.84, 3.61, 7.12],
                  [6.37, 6.71, 5.42, 7.29, 2.45],[6.74, 5.25, 3.5, 2.86, 5.59],[4.95, 2.23, 3.01, 5.91, 2.32],
                  [6.77, 5.99, 4.09, 1.24, 8.95],[2.41, 9.24, 2.48, 8.68, 3.79],[6.67, 6.18, 6.81, 1.07, 7.67],
                  [4.76, 4.25, 5.25, 3.06, 6.05],[6.25, 6.79, 4.3, 1.36, 1.46],[5.51, 3.79, 3.82, 9.07, 4.58],
                  [5.3, 3.84, 3.32, 8.05, 4.12],[7.9, 5.44, 1.65, 6.95, 9.05],[1.28, 9.25, 4.93, 1.87, 3.26],
                  [8.17, 9.64, 8.66, 8.94, 7],[4.75, 3.7, 8.6, 2.4, 1.71],[1.97, 1.96, 2.59, 8.96, 3.78],
                  [7.57, 4.63, 7.05, 9.75, 9.23],[6.37, 6.87, 4.91, 7.46, 5.37],[9.08, 5.11, 6.43, 2.72, 6.61],
                  [3.92, 8.63, 6.02, 1.47, 7.86],[4.54, 5.43, 7.52, 1.93, 4.38],[2.89, 2.05, 7.93, 1.07, 2.4],
                  [6.09, 5.58, 2.84, 3.08, 2.72],[5.96, 3.26, 2.57, 1.59, 8.58],[2.56, 1.7, 6.85, 9.7, 8.89],
                  [7.11, 4.83, 5.6, 8.37, 1.93],[3.98, 6.02, 6.57, 9.22, 7],[7.66, 2.84, 0.51, 7.68, 7.23],
                  [5.95, 2.7, 9.69, 7.42, 5.22],[4.82, 9.48, 9.54, 8, 1.23],[1.65, 3.53, 2.73, 9.58, 8.99],
                  [6.31, 9.24, 5.21, 4.12, 7.75],[2.83, 4.78, 6.37, 8.57, 7.58],[9.93, 9.3, 1.52, 3.73, 7.11],
                  [3.3, 6.1, 5.7, 2.3, 2.98],[7.15, 4.06, 6.88, 9.93, 1.02],[7.2, 8.4, 2.7, 5.9, 2.43],
                  [6.59, 1.96, 8.07, 7.86, 5.86],[7.44, 8.9, 3.74, 3.53, 7.24],[9.48, 2.25, 6, 6.45, 9.98],
                  [1.87, 3.88, 7.62, 1.69, 2.87],[8.16, 5.23, 9.8, 3.78, 8.17],[3.65, 4.39, 7.85, 6.28, 9.97],
                  [1.29, 9.58, 9.57, 5.56, 9.14],[2.35, 8.76, 5.23, 6.82, 5.25],[8.57, 2.88, 2.17, 7.45, 1.16],
                  [4.1, 5.17, 6.84, 6.19, 7.76],[3.69, 2.53, 9.8, 9.31, 1.33],[7.37, 8.17, 4.03, 8.38, 6.43],
                  [4.37, 8.39, 6.88, 9.64, 6.85],[2.47, 8.76, 7.93, 9.94, 5.19],[1.11, 2.25, 6.61, 3.9, 9.23],
                  [2.45, 6.58, 2.01, 1.55, 3.82],[1.97, 6.67, 7.3, 2.01, 8.71],[1.64, 6.58, 4.94, 7.47, 7.31],
                  [8.72, 7.8, 3.26, 7.24, 8.87],[9.98, 1.14, 5.9, 6.83, 5.48],[4.3, 4.24, 3.91, 1.5, 6.26],
                  [6.38, 9.57, 8.35, 9.62, 6.6],[1.66, 2.87, 5.42, 3.45, 3.7],[7.68, 5.11,5.12,8.1,1.04],
                  [9.05,5.48,4.84,9.94,0.74],[7.31,4.95,9.68,3.06,1.53],[8.27,7.44,4.89,1.75,6.22],
                  [1.01,8.5,4.03,7.43,5.32],[9.19,1.65,1.98,3.14,6.69],[7.86,9.23,5.47,8.03,9.52],
                  [1.85,7.19,3.86,7.99,3.2],[6.73,9.94,6.12,6.38,1.66]])

pesos = np.array([2, 2, 4, 1, 1])              
```
@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor4.sh" })

::: Solução
``` python
import numpy as np

notas = np.array([[9.28,0.93,3.92,8.98,3.7],[9.1,5.04,3.68,0.22,8.86],[6.83,3.79,9.39,2.59,7.12],
                  [8.92,1.72,7.85,1.08,5.27], [8.25,4.56,4.54,9.13,9.88],[4.39,5.48,3.26,8.08,3.78],
                  [6.32,4.09,9.45,4.8,7.39],[4.51, 0.61,2.74,4.25,8.67], [5.1,9.4,4.05,5.42,0.51],
                  [0.45,2.18,7.47,6.44,1.76],[2.35,5.73,1.59,2.07,0.82],[1.53,6.04,5.98,3.97,5.53],
                  [5.8,7.68,1.53,7.28,1.32],[3.93,7.79,8.56,1.09,3.78],[8.42,1.53,8.53,9.88,3],
                  [0.88,0.39,8.23,8.1,7.57],[2.7,3.72,4.29,9.66,1.68],[4.97,7.83,6.53,1.89,8.22],
                  [7.94,4.97,6.54,2.6,3.93],[4.9,7.44,4.31,9.57,9.86],[1.09,4.73,4.81,2.92,4.72],
                  [7.61,3.52,6.4,9.98,8.27],[9.19,4.38,3,5.9,8.81],[0.92,0.92,0.67,4.88,6.66],
                  [6.39,1.85,2,6.91,4.13],[3.65,0.41,2.95,6.05,7.91],[6.29,7.34,1.34,3.02,8.8],
                  [6.25,4.2,3.25,6.14,6.21],[9.2,9.73,5.42,5.5,1.92],[0.1,6.77,1.85,7.6,0.21],
                  [4.37,4.29,9.42,9,0.73],[5.1,9.38,8.84,3.92,9.4],[10,5.54,7.37,6.74,10],
                  [5.35,4.83,6.8,6.98,7.08],[8.03,6.59,7.44,7.38,4.74],[7.88,8.21,6.17,6.07,9.11],
                  [3.88,5.93,6.87,4.25,2.61],[5.41,5.13,5.83,7.85,4.09],[4.48,9.1,2.84,6.65,3.08],
                  [5.04,2.03,6.73,4.7,3.56],[5.32,7.37,8.01,8.23,2.2],[6.82,9.31,7.44,3.08,3.65],
                  [1.26,6.3,6.44,7.69,7.07],[7.9,8.75,2.47,2.69,4.43],[4.33,7.45,8.04,2.88,9.06],
                  [2.38, 1.21, 5.12, 1.25, 3.86],[5.39, 1.62, 2.14, 7.41, 1.79],[4.72,2.52,7.76,4.47,6.07],
                  [8.59,4.52,3.07,5.42,3.36],[5.42,7.35,5.26,3.95,1.95],[4.92, 9.76, 1.3, 0.6, 4.45],
                  [5.37, 9.76, 8.55, 6.65, 9.99],[6.52, 5.43, 3.28, 8.59, 8.75],[5.52, 7.29, 2.04, 1.84, 7.39],
                  [8.85, 3.07, 3.66, 8.76, 6.22],[9.63, 8.75, 2.43, 2.65, 05.61],[8.34, 7.36, 1.31, 9.31, 1.03],
                  [2.1, 8.42, 1.32, 1.17, 9.97],[9.97, 4, 3.01, 4.26, 1.16],[2.2, 2.64, 8.94, 9.57, 7.67],
                  [6.57, 9.05, 4.75, 6.81, 9.11],[8.3, 2.52, 4.47, 4.82, 6.67],[7.09, 5.35, 3.99, 0.25, 8.04],
                  [6.84, 7.81, 6, 5.69, 8.57],[3.52, 3.64, 7.31, 9.84, 6.04],[8.89, 6.68, 1.99, 3.02, 9.83],
                  [1.26, 8.25, 1.9, 6.32, 6.84],[7.54, 2.07, 2.18, 9.84, 1.93],[2.84, 2.76, 1.84, 3.52, 9.3],
                  [9.04, 3.23, 1.02, 7.71, 7.75],[4.7, 7.15, 8.36, 2.36, 4.88],[5.76, 5.24, 4.57, 7.11, 0.41],
                  [1.36, 1.12, 2.65, 1.86, 7.96],[3.31, 9.42, 4.46, 4.28, 2.86],[6.55, 6.81, 4.87, 9.26, 6.82],
                  [1.33, 5.69, 5.36, 4.96, 8.33],[9.76, 9.17, 4.96, 9.61, 7.03],[7.62, 2.75, 8.35, 4.79, 3.87],
                  [2.82, 3.51, 1.8, 4.81, 8.25],[2.37, 7.19, 6.77, 8.49, 7.77],[4.72, 6.75, 7.67, 2.94, 1.81],
                  [4.03, 5.03, 1.83, 9.69, 7.67],[2.91, 6.97, 9.1, 4.69, 4.9],[8.97, 3.95, 5.77, 8.67, 9.38],
                  [1.7, 5.42, 8.12, 2.79, 8.95],[6.83, 7.74, 9.27, 4.96, 4.92],[2.16, 5.37, 5.38, 9.61, 8.86],
                  [1.28, 4.85, 6.64, 7.36, 2.44],[7.37, 6.19, 9.81, 7.8, 4.83],[7.84, 9.07, 8.11, 7.72, 8.49],
                  [5.48, 9.19, 8.22, 4.77, 8.14],[4, 2.63, 3.67, 4.57, 7.56],[0.6, 8.45, 2.26, 1.69, 1.6],
                  [6.89, 5.84, 6.47, 5.27, 7.27],[6.33, 3.74, 5.85, 8.33, 8.93],[8.38, 3.19, 5.78, 8.99, 7.69],
                  [3.81, 5.33, 6.67, 8.69, 7.33],[6.73, 8.34, 6.07, 1.88, 8.3],[8.88, 1.45, 3.72, 3.93, 6.85],
                  [2.43, 2, 4.21, 5.96, 7.89],[9.82, 6.86, 7.52, 4.59, 5.39],[4.55, 3.91, 0.7, 7.43, 7.97],
                  [0.64, 9.47, 6.67, 2.46, 4.54],[4.57, 9.52, 3.22, 3.26, 3.59],[4.08, 0.46, 4.4, 4.17, 0.27],
                  [4.8, 7.73, 8.06, 3.98, 4.79],[3.03, 2.7, 1.78, 6.31, 8.49],[4.18, 1.71, 7.74, 5.61, 0.72],
                  [5.33, 3.37, 7.89, 2.41, 1.93],[7.49, 7.92, 5.98, 7.94, 8.9],[4.62, 7.83, 7.3, 3.09, 8.46],
                  [2.07, 6.82, 9.32, 3.42, 6.29],[4.73, 9.98, 3.1, 6.39, 8.57],[5.13, 2.22, 9.39, 6.4, 4.66],
                  [7.88, 9, 3.56, 2.62, 4.76],[1.91, 9.09, 5.56, 2.39, 8.86],[8.84, 1.72, 6.87, 6.4, 7.95],
                  [8.53,2.56, 4.45, 7.64, 5.57],[4.44, 3.69, 4.79, 9.17, 6.03],[9.75, 6.7, 7.56, 7.12, 8.88],
                  [5.23, 5.59, 7.62, 9.75, 9.26],[1.02, 8.2, 9.41, 1.92, 2.46],[3.27, 3.42, 1.33, 6.37, 7.47],
                  [2.31, 5.31, 5.9, 4.47, 7.47],[1.46, 6.75, 4.87, 7.66, 8.84],[5.82, 9.27, 6.84, 2.5, 4.39],
                  [9.99, 1.26, 6.96, 1.03, 8.72],[1.46, 4.33, 1.41, 5.78, 4.67],[5.88, 5.98, 9.34, 6.75, 2.6],
                  [9.82, 8.39, 8.36, 2.4, 3.63],[2.76, 3.64, 9.24, 1.91, 6.49],[1.55, 8.71, 4.84, 3.61, 7.12],
                  [6.37, 6.71, 5.42, 7.29, 2.45],[6.74, 5.25, 3.5, 2.86, 5.59],[4.95, 2.23, 3.01, 5.91, 2.32],
                  [6.77, 5.99, 4.09, 1.24, 8.95],[2.41, 9.24, 2.48, 8.68, 3.79],[6.67, 6.18, 6.81, 1.07, 7.67],
                  [4.76, 4.25, 5.25, 3.06, 6.05],[6.25, 6.79, 4.3, 1.36, 1.46],[5.51, 3.79, 3.82, 9.07, 4.58],
                  [5.3, 3.84, 3.32, 8.05, 4.12],[7.9, 5.44, 1.65, 6.95, 9.05],[1.28, 9.25, 4.93, 1.87, 3.26],
                  [8.17, 9.64, 8.66, 8.94, 7],[4.75, 3.7, 8.6, 2.4, 1.71],[1.97, 1.96, 2.59, 8.96, 3.78],
                  [7.57, 4.63, 7.05, 9.75, 9.23],[6.37, 6.87, 4.91, 7.46, 5.37],[9.08, 5.11, 6.43, 2.72, 6.61],
                  [3.92, 8.63, 6.02, 1.47, 7.86],[4.54, 5.43, 7.52, 1.93, 4.38],[2.89, 2.05, 7.93, 1.07, 2.4],
                  [6.09, 5.58, 2.84, 3.08, 2.72],[5.96, 3.26, 2.57, 1.59, 8.58],[2.56, 1.7, 6.85, 9.7, 8.89],
                  [7.11, 4.83, 5.6, 8.37, 1.93],[3.98, 6.02, 6.57, 9.22, 7],[7.66, 2.84, 0.51, 7.68, 7.23],
                  [5.95, 2.7, 9.69, 7.42, 5.22],[4.82, 9.48, 9.54, 8, 1.23],[1.65, 3.53, 2.73, 9.58, 8.99],
                  [6.31, 9.24, 5.21, 4.12, 7.75],[2.83, 4.78, 6.37, 8.57, 7.58],[9.93, 9.3, 1.52, 3.73, 7.11],
                  [3.3, 6.1, 5.7, 2.3, 2.98],[7.15, 4.06, 6.88, 9.93, 1.02],[7.2, 8.4, 2.7, 5.9, 2.43],
                  [6.59, 1.96, 8.07, 7.86, 5.86],[7.44, 8.9, 3.74, 3.53, 7.24],[9.48, 2.25, 6, 6.45, 9.98],
                  [1.87, 3.88, 7.62, 1.69, 2.87],[8.16, 5.23, 9.8, 3.78, 8.17],[3.65, 4.39, 7.85, 6.28, 9.97],
                  [1.29, 9.58, 9.57, 5.56, 9.14],[2.35, 8.76, 5.23, 6.82, 5.25],[8.57, 2.88, 2.17, 7.45, 1.16],
                  [4.1, 5.17, 6.84, 6.19, 7.76],[3.69, 2.53, 9.8, 9.31, 1.33],[7.37, 8.17, 4.03, 8.38, 6.43],
                  [4.37, 8.39, 6.88, 9.64, 6.85],[2.47, 8.76, 7.93, 9.94, 5.19],[1.11, 2.25, 6.61, 3.9, 9.23],
                  [2.45, 6.58, 2.01, 1.55, 3.82],[1.97, 6.67, 7.3, 2.01, 8.71],[1.64, 6.58, 4.94, 7.47, 7.31],
                  [8.72, 7.8, 3.26, 7.24, 8.87],[9.98, 1.14, 5.9, 6.83, 5.48],[4.3, 4.24, 3.91, 1.5, 6.26],
                  [6.38, 9.57, 8.35, 9.62, 6.6],[1.66, 2.87, 5.42, 3.45, 3.7],[7.68, 5.11,5.12,8.1,1.04],
                  [9.05,5.48,4.84,9.94,0.74],[7.31,4.95,9.68,3.06,1.53],[8.27,7.44,4.89,1.75,6.22],
                  [1.01,8.5,4.03,7.43,5.32],[9.19,1.65,1.98,3.14,6.69],[7.86,9.23,5.47,8.03,9.52],
                  [1.85,7.19,3.86,7.99,3.2],[6.73,9.94,6.12,6.38,1.66]])

pesos = np.array([2, 2, 4, 1, 1])
medias =  notas * pesos/10 
medias =(medias.sum(axis=1)).round(2) 
print("Médias = ", medias)
print("Menor média = ", medias.min())
print("Maior média = ", medias.max())
medger = (medias.mean()).round(2)
print("Média Geral = ", medger)
qtde = np.size(medias[medias>= medger], 0)
print("Qtde médias acima da média geral = ", qtde)
```
:::
