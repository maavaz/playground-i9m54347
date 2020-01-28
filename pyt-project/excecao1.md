# Exceção em Python (Continuação)

O comando **try** pode ter mais de um except associado caso o programador queira associar um tratamento para diferentes tipos de errros. O formato geral do comando é:

![excecao](/imagens/try1.png)

### Exemplo
``` python runnable
# Para visualizar as diferentes mensagens troque a ordem de execução dos comandos associados ao comando try
x = 18

y = 'abc'

try:
   print(x / y)                         # Operação aritmética irá gerar um erro (Exceção)      
   print (z)     
except NameError:                        # Exceção caso uma variável não esteja definida
  print("Variável z não foi definida")
except TypeError:                        # Exceção caso as variáveis possuam tipos definidos
  print("erro na execução do comando. Verifique os tipos das variáveis ou zero no denominador")   
```
**OBS:** A operação aritmética de multiplicação entre as duas varáveis acima não produz erro, pois o python considera essa operação como uma operação de repetição de caracteres.

Além de abortar (parar) o programa, muitas vezes esses erros trazem informações técnicas desnecessárias ao usuário final. O **tratamento de exceções** impede que o programa seja abortado (paralisado) e,
permite que o programador substitua as mensagens de erro da linguagem por uma mensagem mais amigável contendo apenas um código do erro. 
Para que isso aconteça, é necessário que o programa "capture" (catch, em inglês) tais erros e trate-os para que a execução não seja abortada.

### Tratamento de Exceção

Em Python, assim como em muitas linguagens, o tratamento de erro é feito na sua forma mais básica com os comandos **try e except**.

Sua forma geral é semelhante a muitas linguagens de alto de nível:

![excecao](/imagens/try2.png)

Exemplo:
``` python runnable
try:
    altura=float(input('Digite sua altura: '))
except:
    print ('você digitou um valor inválido.')
else:
    if altura <= 1.90:
        print('Você foi aprovado para sem seletiva para o time.')
    else:
        print('você pode fazer precisa fazer uma prova seletiva.')

```
No comando **try** é colocado a operação aritmética (comando) e no comando **except**, que só será executado caso haja erro na execução do comando **try**, é colocado "comandos ou mensagens" que tratam o erro caso ocorra. 