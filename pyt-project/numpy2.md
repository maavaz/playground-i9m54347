# Gerando Números Aleatórios

Existem situações que desejamos uma massa de dados grande para realizarmos testes (pex. em economia, TI etc), mas nem sempre disponíveis. Nessas situações, seria interessante termos a possibilidade de criar um conjunto inteiro de números aleatórios. Outras vezes, desejamos simular jogos de azar (pex. Dados, cartas, bingo etc) e, por isso, gostaríamos que fossem gerados números aleatórios. 
A linguagem python pode nos ajudar, pois possui um módulo - **random** que gera números aleatórios. Para isso, é necessário importar esse módulo:
![random](/imagens/random.png)

A função **random()** gera números reais (float) entre 0 (inclusive) e 1 (não incluído) que podem representar a problabilidade de um evento acontecer:
``` python runnable
import random

x = random.random()

print(x)
```
As funções **randrange()** e **randint()** geram aleatoriamente um número inteiro dentro de um intervalo dado pelo usuário. Semelhantemente a função **random()**, o limite inferior do intervalo é incluído, mas o superior não.
``` python runnable
import random

x = random.randint(1,52)

print(x)

x = random.randrange(1,52)

print(x)

```
Podemos também inicializar um array numpy com valores aleatórios. Execute o exemplo abaixo para criar um array 3x3 com números inteiros aleatórios.

``` python runnable
import random
import numpy as np

x = np.random.randint(1,52, (3,3))

print(x)


```
