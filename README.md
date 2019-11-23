# CYK_Algorithm
Nesse repositório temos uma implementação do algoritmo CYK em um notebook jupyter.

Esse notebook abre um arquivo chamado grammar.txt aonde a gramática desejada para o CYK deve estar.
Assume-se que a gramática está na forma normal de Chomsky.
Gramática exemplo:

S => XB | AB
X => AS
A => a
B => b

Após a leitura do txt, é necessário que a 2ª célula seja executada para definir as funções necessárias para o CYK e
a função cyk.

Para executar o algoritmo em uma palavra basta chamar a função cyk passando a palavra como parámetro.

Ex: cyk(palavra_teste).

Essa função retorna uma lista de listas, sendo cada uma dessas listas representa uma linha da derivação.

Visualização:
Para uma melhor visualização, recomendamos o código:

for x in cyk(palavra_teste):
    print(x)

Também é possível passar uma outra gramática como parâmetro:
Ex: cyk(palavra_teste, grammar=gramatica)

Caso a palavra seja uma palavra válida na gramática, na última linha estará o símbolo inicial.

Caso na última linha esteja um símbolo não inicial isso quer dizer que a palavra não pertence a gramática.

Caso a última linha esteja vazia, isso significa que essa palavra também não pertence a gramática.

Caso um símbolo não contido na gramática apareça na palavra uma exceção KeyError será levantada nesse símbolo.
