# LFPC-lab3
This is laboratory Nr.3 to the "LFPC" subject at university. The code converts Context Free Grammar to the Chomsky Normal Form

#### To find the CNF of CFG you should write your grammar in the grammar.txt file. There is already written an example. The grammar you write in the file must respect this form:
1. Write all terminal symbols, one per line
2. After you finish writing the terminal symbols write 'next'
3. Next write all nonterminal symbols, one per line
4. After you finish writing all nonterminal symbols write 'next'
5. Then write all the rules, one per line in the following form: "Symbol -> Symbols". Between arrow and symbols is one space. Empty productions are written with 'e', for example 'B -> e'.
6. The last line should be written 'next' and Enter
7. Save the grammar.txt

#### Example:
###### a
###### b 
###### next
###### S
###### A
###### B
###### next
###### S -> aA
###### A -> bB
###### B -> ab
###### B -> e
###### next

#### Every block in Main.ipynb represent a function. Every functions' name are maximum explcit, for example: read() -> reading the grammar from grammar.txt, elimintations_of_e_productions -> elimination of every empty production from context free grammar, etc
#### In first block, I imported the combinations function. This function make a list of tuples of all combinations of n. For example, for n = 3, the output is [(1), (2), (3), (1, 2), (1, 3), (2, 3), (1, 2, 3)]. It is used in elimination of e-trasistions.
#### The main block is the last one. In the program are used global variables: terminal_symbols (for storing terminal symbols), nonterminal_symbols (for storiing all nonterminal symbols), rules (for storing the rules of grammar), rules_dic and new_rules_dic (the dicitionaries where are stored the rules in another form), renamings (is stored all the renamings) and productive(is stored all the productive symbols). There are also another lists, but they are not global, for example 'acces' for storing accesible symbols. After the variables declaration, there are all the functions for transforming Context Free Grammar in Chomsky Normal Form.
#### After running every function there is printef the modiffied dictionary of rules to show what changes have beed made
#### intro(), read(), output_intro_data() - the grammar is read, then is printed the grammar you wrote in the grammar.txt to ensure it is correct.
#### grammar_to_dictionary() - is made the dictionary of rules out of rules list. It is used for further calculations in code. The dictionary is printed.
#### eliminations_of_e_productions() - in this function are eliminated all empty productions and is updated dictionary rules. The dictionary rule is printed.
#### eliminations_of_renamings() - in this function are eliminated all the ranmings and is updated dictionary rules. There is printed the all renamings and dictionary rule.
#### eliminations_of_nonproductive_symbols() - in this function are eliminated all nonproductive symbols. There is printed the list of productive symbols and the modified rules dictionary.
#### eliminations_of_inaccesibile_symbols() - in this function are aliminated all inaccesibile symbols. There is printed the list of accesibile symbols and the modified rules dictionary.
#### terminal_symbol_transformations() - in this function all terminal symbols in production rules are changed to nonterminal symbols and new production rules are added. There is printed the new nonterminal symbols and the modified rules dictionary
#### nonterminal_to_nonterminal_transformations() - the rules which are longer than 2 symbol si splited and is made new rules. The modified rules dictionary is printed
#### display_CNF() - is printed the converted CFG to CNF
