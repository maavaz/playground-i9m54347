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

### ELSE

Você pode usar a clausula **ELSE** para definir um bloco de comandos que será executado caso o comando **try** não capture erro algum.  
Sua forma geral é:

![excecao](/imagens/try2.png)

Exemplo:
@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor.sh" })

 ### FINNALY
 
 Você pode usar a clausula **Finnaly** que, se especificada, será executado independentemente se o comando **try** capturar um erro ou não.
 Sua forma geral é:
 
 ![excecao](/imagens/try2.png)
 
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
