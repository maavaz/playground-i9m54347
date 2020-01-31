#Exercitando

``` python
try:
    x/y
except:
    print("Erro na Divisão!!")
else:    
    print("Deu certo!!")
finally:    
    print("FIM!!")
```
?[O trecho de código acima é válido?](single)
-[X] Sim
-[ ] Não, a cláusula "finally" não pode ser usada com "except" 
-[ ] Não, a cláusula "else" não pode ser usada com "except"
-[ ] Não, as cláusulas "finally" e "else" não podem ser usadas juntas

?[Ainda com relação ao trecho de código acima, qual o resultado da sua execução?](single)
-[ ] Erro de Sinataxe!!
-[ ] Exibe a mensagem: "Erro de Divisão!!" 
-[ ] Exibe a mensagem: "Deu Certo" e em seguida a mensagem: "FIM!!"
-[x] Exibe a mensagem: "Erro de Divisão!!" e em seguida a mensagem: "FIM!!"

``` phyton
try:
    print(5 == 6)
except ValueError:
    print('ValueError')
finally:
    print('finally')
``` 
?[Qual o resultado da execução do trecho de código acima?](single)
-[ ] Exibe a mensagem: "5 == 6"
-[ ] Exibe a mensagem: "ValueError" 
-[x] Exibe a mensagem: "false" e em seguida a mensagem: "finally"
-[ ] Exibe a mensagem: "ValueError" e em seguida a mensagem: "finally"

?[Quantas cláuslas "except" um bloco de comando "try-except" pode ter?](single)
-[ ] zero
-[ ] Umu
-[ ] mais de uma cláusula
-[x] maior que zero

### Exercício 1
Faça um programa que solicite ao usuário 2 números inteiros. A seguir, calcule e mostre a divisão do primeiro pelo segundo. 
Obrigatório a inclusão do bloco **try-except** nas leituras (ValueError) e no cálculo da divisão (ZeroDivisionError). O programa deve ter também a clásula **"finally"** com a mensagem "FIM!!". Atenção: O programa só continua se não houver erro.

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor3.sh" })

::: Solução
``` python
try:
  numero1 = int(input('Digite um número:'))
except ValueError:
    print('Erro na digitação do primeiro número')
else:    
  try:
    numero2 = int(input('Digite outro número:'))
  except ValueError:
    print('Erro na digitação do segundo número')
  else:
    try:  
      divisao = numero1 / numero2
    except ZeroDivisionError:
      print('Erro Divisão por zero!!')   
    else:    
      print('Divisão = ', divisao)  
finally:
      print("FIM!!")  
```
