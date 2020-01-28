# Exceção em Python

Uma **exceção** é algo inesperado, fora do planejado que ocorre durante a execução de um programa. Por exemplo, você quer realizar alguma operação aritmética (uma divisão) envolvendo dois números, 
mas acaba digitando uma letra no lugar de um dos números, o python irá gerar um erro na execução dessa operação(comando), chamado de **exceção**. 

### Exemplo
``` python runnable
x = 18

y = 'abc'

print(x / y)    # Operação aritmética irá gerar um erro (Exceção)

```
**OBS:** A operação aritmética de multiplicação entre as duas varáveis acima não produz erro, pois o python considera essa operação como uma operação de repetição de caracteres.

Além de abortar (parar) o programa, muitas vezes esses erros trazem informações técnicas desnecessárias ao usuário final. O **tratamento de exceções** impede que o programa seja abortado (paralisado) e,
permite que o programador substitua as mensagens de erro da linguagem por uma mensagem mais amigável contendo apenas um código do erro. 
Para que isso aconteça, é necessário que o programa "capture" (catch, em inglês) tais erros e trate-os para que a execução não seja abortada.

### Tratamento de Exceção

Em Python, assim como em muitas linguagens, o tratamento de erro é feito na sua forma mais básica com os comandos **try e except**.

Sua forma geral é semelhante a muitas linguagens de alto de nível:

![excecao](/imagens/try.png)

Voltando a código anterior, vamos filtrar esse erro:
``` python
In [4]: try:
   ...:     x / y
   ...: except:    
   ...:     print("erro na execução do comando. Verifique os tipos das variáveis ou zero no denominador")
   ...: 
   
>>>  erro na execução do comando. Verifique os tipos das variáveis ou zero no denominador

```
No comando **try** é colocado o comando e no comando **except**, que só será executado caso haja erro na execução do comando **try**, é colocado "comandos ou mensagens" que tratam o erro caso ocorra. 
