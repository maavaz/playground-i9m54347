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
-[ ] imprime a mensagem: "Erro de Divisão!!" 
-[ ] imprime a mensagem: "Deu Certo", seguida da mensagem: "FIM!!"
-[x] imprime a mensagem: "Erro de Divisão!!", seguida da mensagem: "FIM!!"
