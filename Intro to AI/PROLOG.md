# Semantics
## Basics
- `Head :- Body.`
- Clauses with empty bodies are called *facts*
$$
cat(tom).
$$
- Clauses with bodies are called *rules*. Rules describe new rules based on
facts and/or other rules
$$
animal(X) :- cat(X).
$$
- Queries are needed to show outputs. They are also called goals
$$
\begin{matrix}
?- cat(X). \\
Answer: X = tom
\end{matrix}
$$
## Rules
$$father(Y,Z) \text{ :- } man(Y), son(Z,Y).$$
- If the body of the rule is true then the head is true
- ":-" is read as "if"
- "," is logical AND
- ";" is logical OR
- The statement is read as: $Y$ is a father of $Z$ if $Y$ is a man and $Z$ is a son of $Y$.
- Note that order and semantics of the arguments are specified by programmer
	- By $father(Y,Z)$ we can mean that $Y$ is a father of $Z$ OR $Z$ is father of $Y$
## Datatypes
Prolog's single data type is the term. There are 4 term types:
- **Atoms**
	- An atom is a general-purpose name with no inherent meaning
	- Should begin with a lowercase letter or should be surrounded by single quotes
	- May contain uppercase letters, lowercase letters, digits (0-9), characters (+-*/<>=:~)
	- Examples:
		- `cat, ‘Dog’, ‘another cat’, my_pet, my`
- **Numbers** (integers and floats)
- **Variables**
	- Variables consists of letters, digits and underscores. Variables start with uppercase letter or underscore
	- Examples:
		- `X, _Y, Piano, Person_1, DOLL`
	- Free variable is the one, for which the value was not assigned, bound is the opposite
		- `?- 5 = 4 // false`
		- `?- X = 5, X = 4 // false`
		- `?- X = 5 + 4 // it is not a mathematical expression!`
		- `?- X is 5 + 4 // X = 9`
		- `?- X = Y, X = 5, Z is Y + 4 // X = 5, Y = 5, Z = 9`
	- Anonymous variable `‘_’` makes the output for that variable invisible
		- ?- father(X,_). // should return all fathers X without showing names of children
- **Compound terms**
	- A compound term is composed of an atom called a "functor" and a number of "arguments", which are again terms
	- Compound terms are ordinarily written as a functor followed by a comma-separated list of argument terms, which is contained in parentheses
	- The number of arguments is called the term's arity. An atom can be regarded as a compound term with arity zero
	- Examples:
		- `friend(max,peter).`
		- `person_friends(zelda,[tom,jim])`
- **List**
	- A list is an ordered collection of terms. It is denoted by square brackets with the terms separated by commas
	- It is a compound term type
	- Examples:
		- `[1,2,3]`
		- `[1]`
		- `[]`
		- `[red,green,blue].`
- **Strings**
	- String is a sequence of characters surrounded by double quote
	- It is equivalent to either a list of (numeric) character codes, a list of characters (atoms of length 1), or an atom depending on the value of the Prolog flag double quotes
	- It is a compound term type
		- Examples:
			- `"to be, or not to be"`
## Useful operators
- Negation: `not(term)` or `\+` term
	- `female(X) :- not(male(X)).`
	- `legal(X) :- \+ illegal(X).`
- Not equal: `\=`
	- X`\=`Y
- Cut: !
	- Takes only the first result
	- `?- parent(Y,X), !. // E`
# References
References
1. [Wikipedia](https://en.wikipedia.org/wiki/Prolog)
2. [A Taste of Prolog by Aja Hammer](https://confreaks.tv/videos/cascadiaruby2012-a-taste-of-prolog)
