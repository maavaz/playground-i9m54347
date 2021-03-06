# Exceção em Python (Continuação)

### <b> Tipos de Erros (Except) </b>

Tratar qualquer tipo de exceção da mesma maneira não é considerado uma boa prática de programação. É recomendável especificar o tipo de erro exato que a cláusula **except** irá capturar. Por isso, o comando **try** pode ter mais de um **except** associado ao tipo de errro, caso o programador queira associar um tratamento diferente para cada um deles. 

O formato geral do comando é:

![excecao](/imagens/try1.png)

Alguns tipos de exceção mais comuns:

+ <b>NameError:</b> exceção gerada quando o programa não consegue encontrar um nome de variável local ou global.  
+ <b>TypeError:</b> exceção gerada quando é passado um objeto de um tipo diferente do tipo que a função espera como argumento. 
+ <b>ValueError:</b> essa exceção ocorre quando um argumento de uma função tem o tipo certo, mas um valor inadequado.
+ <b>ZeroDivisionError:</b> exceção gerada quando você fornece um zero como segundo argumento para uma divisão ou módulo.
+ <b>FileNotFoundError:</b> essa exceção é gerada quando o arquivo ou diretório que o programa solicitou não existe.

### <b> Exemplo </b>
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
  print("Erro de execução do comando. Verifique os tipos das variáveis ou zero no denominador")   
```

### <b> ELSE </b>

Você pode usar a clausula **ELSE** para definir um bloco de comandos que será executado caso o comando **try** não capture erro algum.  
Sua forma geral é:

![excecao](/imagens/try2.png)

Exemplo:
@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor.sh" })

 ### <b> FINNALY </b>
 
 Você pode usar a clausula **Finnaly** que, se especificada, será executado independentemente se o comando **try** capturar um erro ou não.
 Sua forma geral é:
 
 ![excecao](/imagens/try3.png)
 
 Exemplo:
 ``` python runnable
 # Execute retirando o símbolo de comentário (#) da linha que contém o comando x = 10
 
 #x = 10
 try:
  print(x)
except:
  print("A variável x não foi definida")
finally:
  print("Eu exibo a mensagem em qualquer condição")
