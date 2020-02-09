# Exercitando

?[Qual dos caracteres abaixo, colocados numa expressão regex mapeia zero ou mais caracters?](single)
-[ ] $
-[ ] + 
-[x] *
-[ ] .

?[O que faz a expressão regular: [a-z]?](single)
-[ ] Verifica e retorna apenas os caracteres a e z, se existirem
-[ ] Verifica e retorna os caracteres de a até z e de A até Z, se existirem
-[ ] Verifica e retorna os caracteres de A até Z, se existirem
-[x] Verifica e retorna os caracteres de a até z

?[Qual das expressões regulares abaixo, verifica e retorna todas as palavras da String: "aviao aviador aviacao"?](single)
-[ ] "avia[a-z]$"
-[ ] "avia[a-z]."
-[x] "avia[a-z]*"
-[ ] "avia[^a-z]"

?[Qual das expressões regulares abaixo, verifica e retorna as strings "aviao ou barco" ou os dois?](single)
-[x] "aviao | barco"
-[ ] "aviao ou barco"
-[ ] "aviao $ barco"
-[ ] "aviao & barco"

?[O que faz a expressão regular:"\d{3}" ?](single)
-[ ] Verifica e retorna o caracter "d", se estiver na terceira posição da sequência
-[ ] Verifica e retorna as sequências de strings que iniciam com a letra "d", se existirem
-[ ] Verifica e retorna uma sequência de 3 letras "d", se existirem
-[x] verifica e retorna qualquer sequência de 3 dígitos

?[O que deve ser colocado após um determinado caracter para que retorne uma sequência de 1 até 3 desse caractere" ?](single)
-[X] {1,3}
-[ ] {1-3}
-[ ] {1 3}
-[ ] [1-3]

``` python
sentenca = 'nos nao estamos nas nuvens'
resultado = re.findall(r'\bn.s', sentenca)
print(resultado)
```
?[Dado o trecho de código acima, qual o resultado de sua execução?](single)
-[x] ['nos', 'nas']
-[ ] ['nos', 'nas', 'nuvens']
-[ ] ['nos', 'nao', 'nas', 'nuvens']
-[ ] ['nos']
