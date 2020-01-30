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
