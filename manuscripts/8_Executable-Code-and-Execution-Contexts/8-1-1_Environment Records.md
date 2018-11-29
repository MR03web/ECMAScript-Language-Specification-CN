# 8.1.1 Environment Records

There are two primary kinds of *Environment Record* values used in this specification: *declarative Environment Records* and *object Environment Records*. Declarative Environment Records are used to define the effect of ECMAScript language syntactic elements such as *FunctionDeclarations*, *VariableDeclarations*, and *Catch* clauses that directly associate identifier bindings with ECMAScript language values. Object Environment Records are used to define the effect of ECMAScript elements such as *WithStatement* that associate identifier bindings with the properties of some object. Global Environment Records and function Environment Records are specializations that are used for specifically for *Script* global declarations and for top-level declarations within functions.

在本标准中，共有两类环境记录项：声明环境记录项和对象环境记录项。声明环境记录项用于定义ECMAScript语言语法元素的效果，例如*FunctionDeclarations*、*VariableDeclarations*和*Catch*子句，它们直接将标识符和ECMAScript语言值绑定。对象环境记录用于定义ECMAScript元素的效果，例如*WithStatement*将标识符绑定与某个对象的属性相关联。全局环境记录项和函数环境记录项是专门用于*Script*全局声明和函数内的顶级声明。

For specification purposes Environment Record values are values of the Record specification type and can be thought of as existing in a simple object-oriented hierarchy where Environment Record is an abstract class with three concrete subclasses, declarative Environment Record, object Environment Record, and global Environment Record. Function Environment Records and module Environment Records are subclasses of declarative Environment Record. The abstract class includes the abstract specification methods defined in Table 14. These abstract methods have distinct concrete algorithms for each of the concrete subclasses.

出于规范目的，环境记录项的值是记录规范类型的值，可以将环境记录项理解为一个简单的面向对象式的继承结构，环境记录项是一个有三个实现类的抽象类，即声明环境记录，对象环境记录和全局环境记录。函数环境记录和模块环境记录是声明环境记录的子类。表14是这个抽象类的抽象方法. 对于每个实现类，这些抽象方法具有不同的算法。

Method 方法 | Purpose 目的
------------ | -------------
HasBinding(N) | /
CreateMutableBinding(N,D) | /