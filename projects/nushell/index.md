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

To solve this problem, I decided to parse bash's grammar and add rules to allow for rules that would be considered "more intuitive", coming from someone with greater familiarity with python or C.

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

### `ply`ing a grammar

Now that ANTLR4 was set up and ready to go, it was time to find a grammar that could be used to parse Bash. I found not only one, but two different grammars! This made consolidating rules about the grammar easier to understand. 