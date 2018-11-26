# 8.1 Lexical Environments 词法环境

A *Lexical Environment* is a specification type used to define the association of *Identifiers* to specific variables and functions based upon the lexical nesting structure of ECMAScript code. A Lexical Environment consists of an Environment Record and a possibly null reference to an *outer* Lexical Environment. Usually a Lexical Environment is associated with some specific syntactic structure of ECMAScript code such as a *FunctionDeclaration*, a *BlockStatement*, or a *Catch* clause of a *TryStatement* and a new Lexical Environment is created each time such code is evaluated.

词法环境是一种规范类型，用于根据ECMAScript代码的词法嵌套结构，定义特定变量和函数标识符间的关联。一个词法环境由一个环境记录项和一个可能为空的外部词法环境引用构成。通常词法环境会与一些特定的语法结构相联系。例如*FunctionDeclaration*、*BlockStatement*或者*TryStatement*的*Catch*，每次遇到像这样的代码时都会有一个新的词法环境被创建出来。

An Environment Record records the identifier bindings that are created within the scope of its associated Lexical Environment. It is referred to as the Lexical Environment's *EnvironmentRecord*.