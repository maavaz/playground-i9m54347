# Expressões Regulares (Continuação)

### Metacaracters
Metacaracteres corresponde a um conjunto de caracteres que possuem um signficado expecífico e que são interpretados de maneira especial pelo mecanismo RegEx:

![regex](/imagens/regex.png)

### Caracter []
``` python

padrao = '[rst]'
texto='Bom programador? ler e interpretar textos aprender conceitos, não decorar comandos e fazer muitos exercícios'
#Procurar os caracteres "r,s,t" no texto e retorna uma lista.
resultado = re.findall(padrao, texto) 
print('Resultado: ', resultado)
```
**Resultado:"" 
['r', 'r', 'r', 'r', 't', 'r', 'r', 't', 'r', 't', 't', 's', 'r', 'r', 't', 's', 'r', 'r', 's', 'r', 't', 's', 'r', 's']

O padrão [rst] irá retornar uma lista contendo os caracteres r,s,t .
Pode-se especificar o intervalo utilizando o caracter hífen para serar os extremos, por exemplo;
[r-t]  = [rst]
[1-3]  = [123] 
[0-27] = [0127].

O caracter ^ funciona como a negação da sequência informada se for colocado no início sa sequência entre colchetes:
[^abc] significa qualquer caracter com exceção de a, b ou c.
[^0-9] significa qualquer caracter não-dígito.
