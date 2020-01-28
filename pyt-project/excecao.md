# Exceção em Python

Uma exceção é algo inesperado, fora do planejado que ocorre durante a execução de um programa. Por exemplo, você quer realizar uma operação aritmética envolvendo dois números, 
mas acaba digitando uma letra no lugar de um dos números, o python irá gerar um erro, chamado **exceção**. 

### Exemplo
``` python
In [1]: x = 18

In [2]: y = 'abc'

In [3]: x / y    # Operação aritmética irá gerar um erro
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-4-1994261362eb> in <module>()
----> 1 x / y    # Operação aritmética irá gerar um erro

TypeError: unsupported operand type(s) for /: 'int' and 'str'

```
Além de abortar (parar) o programa, muitas vezes esses erros trazem informações técnicas desnecessárias ao usuário final. O **tratamento de exceções** possibilita que o programa seja abortado (paralisado) e,
permite que o programador substitua as mensagens de erro da linguagem por uma mensagem mais amigável contendo apenas um código do erro. O
 

Um programa bem elaborado precisa capturar (catch, em inglês) tais objetos e tratá-los para que a execução não seja abortada
