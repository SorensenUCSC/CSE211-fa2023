---
title: "NuShell: Modifying Bash's grammar to allow for saner syntax"
layout: single
classes: wide
---




### Author

Ananth ("Ant") Srikanth [@Ant-28](https://github.com/Ant-28)\

## Introduction

Bash is ubiquitous with shell scripting, with some or the other form of the shell being an inextricable part of the command-line experience for users of UNIX(-like) systems. However, it is riddled with frustrating syntax and confusing shorthand that leaves people, more often than not, searching up how to write a specific command.
Furthermore, coming from most programming languages, Bash tends to introduce inconveniences (e.g. the fact that spaces are not allowed in an assignment statement, more on this later.) 

This does not mean Bash is outright awful. Piping syntax is easy to understand and familiarizing oneself with it doesn't take too long.

To solve these problems, I decided to parse bash's grammar and add rules to allow for rules that would be considered "more intuitive", coming from someone with greater familiarity with python or C. This project can take in a file in this "modified bash syntax" and spits out Bash that an interpreter can execute. 

## Procedure

To parse bash, I decided to use the Antlr4 parser generator. Why? Rather than writing a function for each grammar rule in `ply`, I only needed to write the grammar once in BNF form. Additionally, ANTLR supports loading in tokens using a token file, so tokens only need to be written down once. I decided to also use a Python backend since it was simpler than trying to set up ANTLR for Java or C++.

![ANTLR4 Diagram](images/antlr1.png)

### Setting Up ANTLR4

After installing the ANTLR jar files, I added the following to my `.bashrc`:

```bash
# some more ls aliases
export CLASSPATH=".:/usr/local/lib/antlr-4.9.3-complete.jar:$CLASSPATH"
# simplify the use of the tool to generate lexer and parser
alias antlr4='java -Xmx500M -cp "/usr/local/lib/antlr-4.9.3-complete.jar:$CLASSPATH" org.antlr.v4.Tool'
# simplify the use of the tool to test the generated code
alias grun='java -Xmx500M -cp "/usr/local/lib/antlr-4.9.3-complete.jar:$CLASSPATH" org.antlr.v4.gui.TestRig'
```

This greatly simplifies ANTLR4 execution since `antlr4` needs to be called every time the lexer and parser are generated.

### `ply`ing a grammar (no pun intended)

Now that ANTLR4 was set up and ready to go, it was time to find a grammar that could be used to parse Bash. I found not only one, but two different grammars! This made consolidating rules about the grammar easier to understand. 
[The first grammar](https://cmdse.github.io/pages/appendix/bash-grammar.html) I found was in standard BNF form, angle brackets and all. I attempted to convert this to a grammar that ANTLR4 would accept, with little success when parsing. 
![**Bash Grammar**](images/bashgram1.png)

My big break was when I found an alternate formal grammar [here](https://pubs.opengroup.org/onlinepubs/9699919799.2016edition/utilities/V3_chap02.html#tag_18_10). This also included separate rules for loops (for and while), as well as if statements, making it much easier to parse. After a bit of tweaking, I was able to create a parser file:

```antlr
program          : linebreak complete_commands linebreak
                 | linebreak
                 ;
complete_commands: complete_commands newline_list complete_command
                 |                                complete_command
                 ;
complete_command : nlist separator_op
                 | nlist
                 ;
nlist             : nlist separator_op and_or
                 |                   and_or
                 ;
```

Note that some production rules had to be modified, like the list keyword since `list` is also a keyword in Python. 

After some testing and rule modification, the parser worked! However, it was missing some terms, 