# yacc

## definition

- Define tokens followed by `%token`. And then macros are going to be defined in a **`*.tab.h`**
- Include **`*.tab.h`** in a lex file so that Lex can use those tokens
- This section is going to be copied to **`*.tab.c`** as is.

## rules

In this section, we can write BNF-like parser.
And we can get values from lex

- How to pass values from lex to yacc
    - Write **`return value;`** in the action section of a lex file. Default type is `int`
    - Assign a value to **`yylval`** variable in a lex file. Default type is `int`
- How to get values from lex
    - symbols
        - $$: lval symbol
        - $1: The first rval symbol
        - $2: The second rval symbol

## subroutines

- This section is going to be copied to **`*.tab.c`** as is.
- `yylex` function is called `yyparse`.
