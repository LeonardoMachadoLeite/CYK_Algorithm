# CYK_Algorithm
Nesse repositório temos uma implementação do algoritmo CYK em um notbeook jupyter

Esse notebook abre um arquivo chamado grammar.txt aonde a gramática desejada para o CYK deve estar.
Assume-se que a gramática está na forma normal de Chomsky.
Gramática exemplo:

S => XB | AB
X => AS
A => a
B => b

Após a leitura do txt, é necessário que a 2ª célula seja executada para definir as funções necessárias para o CYK e
a função cyk.

Para executar o algoritmo em uma palavra basta chamar a função cyk passando a palvara como parámetro.
Ex: cyk(palavra_teste)
Essa função retorna uma lista de listas, sendo cada uma dessas listas representa uma linha da derivação.

Visualização:
Para uma melhor visualização, recomendamos o código:

for x in cyk(palavra_teste):
    print(x)

Também é possível passar uma outra gramática como parâmetro:
Ex: cyk(palavra_teste, grammar=gramatica)
