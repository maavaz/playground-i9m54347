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

### Desafio
#Dada a lista abaixo, crie 2 listas, sem repetições, contendo os nomes (lnomes) e os provedores (lprovedor). Ao final, imprima as listas.

enderecos = ['<rjlowe@uct.ac.za>' , '<josrodri@caret.cam.ac.uk>', '<stephen.marquard@gmail.com>', '<zqian@iupui.edu>', '<gopal.ramasammycook@nakamura.uits.iupui.edu>', '<david.horwitz@collab.sakaiproject.org>', '<antranig@umich.edu>'
, '<dhorwitz@collab.sakaiproject.org>', '<rjlowe@media.berkeley.edu>', '<cwen@media.berkeley.edu>', '<ray@gmail.com>', '<louis@gmail.com>',  '<gsilver@media.berkeley.edu>', '<josrodri@caret.cam.ac.uk>', '<gopal.ramasammycook@nakamura.uits.iupui.edu>']

@[Programacao Python]({"stubs": ["./www/editor"],"command": "sh /project/target/www/editor5.sh" })
::: Solução
```python
import re
enderecos = ['<rjlowe@uct.ac.za>' , '<josrodri@caret.cam.ac.uk>', '<stephen.marquard@gmail.com>', '<zqian@iupui.edu>', '<gopal.ramasammycook@nakamura.uits.iupui.edu>', '<david.horwitz@collab.sakaiproject.org>', '<antranig@umich.edu>'
, '<dhorwitz@collab.sakaiproject.org>', '<rjlowe@media.berkeley.edu>', '<cwen@media.berkeley.edu>', '<ray@gmail.com>', '<louis@gmail.com>',  '<gsilver@media.berkeley.edu>', '<josrodri@caret.cam.ac.uk>', '<gopal.ramasammycook@nakamura.uits.iupui.edu>']

lnomes = set()   #Cria um conjunto pois não tem elementos repetidos
lprovedor = set()
for x in enderecos:
    sem = str((x.strip('<')).strip('>')) #Retira o  <> e retorna a string do endereço de email
    quebra = sem.split('@')              # Quebra a string sem no @    
    print(sem)  
    lnomes.add(quebra[0])
    lprovedor.add(quebra[1])	

print(lnomes)
print(lprovedor)
```
:::
