# 8.1 Lexical Environments 词法环境

A *Lexical Environment* is a specification type used to define the association of *Identifiers* to specific variables and functions based upon the lexical nesting structure of ECMAScript code. A Lexical Environment consists of an Environment Record and a possibly null reference to an *outer* Lexical Environment. Usually a Lexical Environment is associated with some specific syntactic structure of ECMAScript code such as a *FunctionDeclaration*, a *BlockStatement*, or a *Catch* clause of a *TryStatement* and a new Lexical Environment is created each time such code is evaluated.

词法环境是一种规范类型。用于

A * Lexical Environment *是一种规范类型，用于根据ECMAScript代码的词法嵌套结构定义* Identifiers *与特定变量和函数的关联。 词汇环境由环境记录和可能为* * *词汇环境的空引用组成。 通常，词汇环境与ECMAScript代码的某些特定语法结构相关联，例如* TryStatement *的* FunctionDeclaration *，* BlockStatement *或* Catch *子句，并且每次评估此类代码时都会创建新的词法环境。

词法环境 是一个用于定义特定变量和函数标识符在 ECMAScript 代码的词法
嵌套结构上关联关系的规范类型。一个词法环境由一个环境记录项和可能为空的
外部词法环境引用构成。通常词法环境会与特定的 ECMAScript 代码诸如
FunctionDeclaration,WithStatement 或者 TryStatement 的 Catch 块这样的
语法结构相联系，且类似代码每次执行都会有一个新的语法环境被创建出来。