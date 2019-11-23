In this repository we have an implementation of the CYK algorithm in a notbeook jupyter.

This notebook opens a file called grammar.txt where the desired grammar for CYK should be.
The grammar is assumed to be in the normal form of Chomsky.
Grammar example:

S => XB | AB
X => AS
A => a
B => b

After reading the txt, it is necessary that the 2nd cell is executed to define the necessary functions for CYK and
the cyk function.

To execute the algorithm in a word just call the function cyk passing the word as a parameter.
Ex: cyk (test_word)
This function returns a list of lists, each of which lists represents one line of the derivation.

Preview:
For a better view, we recommend the code:

for x in cyk (test_word):
    print (x)

You can also pass another grammar as a parameter:
Ex: cyk (test_word, grammar = grammar)

If the word is a valid word in grammar, on the last line is the starting symbol.

If in the last line is a non-initial symbol this means that the word does not belong to grammar.

If the last line is empty, that means that word does not belong in grammar either.

If a symbol not contained in the grammar appears in the word a KeyError exception will be raised in that symbol.
