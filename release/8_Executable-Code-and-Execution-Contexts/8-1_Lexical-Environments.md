# 8.1 Lexical Environments 词法环境

A *Lexical Environment* is a specification type used to define the association of *Identifiers* to specific variables and functions based upon the lexical nesting structure of ECMAScript code. A Lexical Environment consists of an Environment Record and a possibly null reference to an *outer* Lexical Environment. Usually a Lexical Environment is associated with some specific syntactic structure of ECMAScript code such as a *FunctionDeclaration*, a *BlockStatement*, or a *Catch* clause of a *TryStatement* and a new Lexical Environment is created each time such code is evaluated.

词法环境是一种规范类型，用于根据ECMAScript代码的词法嵌套结构，定义特定变量和函数标识符间的关联。一个词法环境由一个环境记录项和一个可能为空的对外部词法环境的引用[^1]构成。通常词法环境会与一些特定的语法结构相联系。例如*FunctionDeclaration*、*BlockStatement*或者*TryStatement*的*Catch*，每次遇到像这样的代码时都会有一个新的词法环境被创建出来。

An Environment Record records the identifier bindings that are created within the scope of its associated Lexical Environment. It is referred to as the Lexical Environment's *EnvironmentRecord*.

环境记录项记录了在其关联的词法环境范围内创建的标识符绑定。它被称为词法环境的*EnvironmentRecord*。

The outer environment reference is used to model the logical nesting of Lexical Environment values. The outer reference of a (inner) Lexical Environment is a reference to the Lexical Environment that logically surrounds the inner Lexical Environment. An outer Lexical Environment may, of course, have its own outer Lexical Environment. A Lexical Environment may serve as the outer environment for multiple inner Lexical Environments. For example, if a *FunctionDeclaration* contains two nested *FunctionDeclarations* then the Lexical Environments of each of the nested functions will have as their outer Lexical Environment the Lexical Environment of the current evaluation of the surrounding function.

OLER用于对词法环境的逻辑嵌套进行建模。一个（内部的）词法环境的OLER，是逻辑上包含这个内部词法环境的词法环境。当然，外部的词法环境可能也有自己的外部词法环境。一个词法环境可以做为多个内部词法环境的外部环境，例如，如果*FunctionDeclaration*包含两个嵌套的*FunctionDeclarations*，那么每个嵌套函数的词法环境都是外部函数本次执行所产生的词法环境。

A *global environment* is a Lexical Environment which does not have an outer environment. The global environment's outer environment reference is null. A global environment's EnvironmentRecord may be prepopulated with identifier bindings and includes an associated global object whose properties provide some of the global environment's identifier bindings. As ECMAScript code is executed, additional properties may be added to the global object and the initial properties may be modified.

*global environment*是一个没有外部环境的词法环境。全局环境的OLER是null。全局环境的环境记录可以预先做标识符绑定。并包含一个关联的全局对象。其属性提供给全局环境进行标识符绑定。在执行ECMAScript时，可以在全局对象上添加属性，并且初始属性可以被修改。

A *module environment* is a Lexical Environment that contains the bindings for the top level declarations of a *Module*. It also contains the bindings that are explicitly imported by the *Module*. The outer environment of a module environment is a global environment.

*module environment*是包含一个*Module*顶级声明绑定的词法环境。它还包含*Module*中显式导入的绑定。模块环境的外部环境是全局环境。

A *function environment* is a Lexical Environment that corresponds to the invocation of an ECMAScript function object. A function environment may establish a new **this** binding. A function environment also captures the state necessary to support **super** method invocations.

*function environment*是对应ECMAScript函数对象调用的词法环境。函数环境可以建立一个新的**this**绑定。函数环境还捕获支持**super**方法调用所需的状态。

Lexical Environments and Environment Record values are purely specification mechanisms and need not correspond to any specific artefact of an ECMAScript implementation. It is impossible for an ECMAScript program to directly access or manipulate such values.

词法环境和环境记录项是纯粹的规范机制，不需要ECMAScript的实现保持一致。ECMAScript程序不能直接访问或操作这些值。

[^1]: 外部（词法）环境引用，后面简写为OLER