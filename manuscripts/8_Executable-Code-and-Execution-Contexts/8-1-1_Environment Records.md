# 8.1.1 Environment Records

There are two primary kinds of *Environment Record* values used in this specification: *declarative Environment Records* and *object Environment Records*. Declarative Environment Records are used to define the effect of ECMAScript language syntactic elements such as *FunctionDeclarations*, *VariableDeclarations*, and *Catch* clauses that directly associate identifier bindings with ECMAScript language values. Object Environment Records are used to define the effect of ECMAScript elements such as *WithStatement* that associate identifier bindings with the properties of some object. Global Environment Records and function Environment Records are specializations that are used for specifically for *Script* global declarations and for top-level declarations within functions.

在本标准中，共有两类环境记录项：声明式环境记录项和对象环境记录项。声明式环境记录项用于定义ECMAScript语言语法元素的效果，例如*FunctionDeclarations*、*VariableDeclarations*和*Catch*子句，它们直接将标识符和ECMAScript语言值绑定。对象环境记录用于定义ECMAScript元素的效果，例如*WithStatement*将标识符绑定与某个对象的属性相关联。全局环境记录项和函数环境记录项是专门用于*Script*全局声明和函数内的顶级声明。

For specification purposes Environment Record values are values of the Record specification type and can be thought of as existing in a simple object-oriented hierarchy where Environment Record is an abstract class with three concrete subclasses, declarative Environment Record, object Environment Record, and global Environment Record. Function Environment Records and module Environment Records are subclasses of declarative Environment Record. The abstract class includes the abstract specification methods defined in Table 14. These abstract methods have distinct concrete algorithms for each of the concrete subclasses.

出于规范目的，环境记录项的值是记录规范类型的值，可以将环境记录项理解为一个简单的面向对象式的继承结构，环境记录项是一个抽象类，它有三个实现类，即声明环境记录，对象环境记录和全局环境记录。函数环境记录和模块环境记录是声明式环境记录的子类。表14是这个抽象类的抽象方法，对于每个实现类，这些抽象方法具有不同的实际算法。

Method 方法 | Purpose 目的
------------ | -------------
HasBinding(N) | 判断环境记录是否包含某个绑定，字符串N是绑定名称文本。包含则返回true，反之返回false。
CreateMutableBinding(N,D) | 在环境记录中创建一个新的但未初始化的可变绑定。字符串值N是绑定的名称文本。如果Boolean类型参数D为true，这之后可以删除绑定
CreateImmutableBinding(N,S) | 在环境记录中创建一个新的但未初始化的不可变绑定。字符串值N是绑定的名称文本。如果S为true，则在初始化后再次设置将抛出异常，无论严格模式如何设置该绑定的引用的操作。
InitializeBinding(N, V) | 设置环境记录中已经存在但没有初始化的绑定的值。字符串值N是绑定的名称文本。V是要设置的绑定的值，可以是任何ECMAScript语言类型的值。S是Boolean flag。 如果S是true，那么绑定无法设置抛出TypeError异常。
GetBindingValue(N, S) | 从环境记录中返回一个已经存在的绑定的值。字符串值N是绑定的名称文本。S用于指定是否为严格模式引用或者需要严格模式的引用语义。如果S为true且该绑定不存在，则抛出ReferenceError异常。如果存在但未初始化，则无论S的值如何，都抛出ReferenceError。
DeleteBinding(N) | 从环境记录项中删除一个绑定。字符串值N是绑定的名称文本。如果存在绑定N，则删除并返回true。如果存在绑定N但无法删除则返回false。如果不存在绑定N则返回true。
HasThisBinding() | 判断环境记录是否建立了**this**绑定。是则返回true，没有则返回false。
HasSuperBinding() | 判断环境记录是否建立了**super**绑定。是则返回true，没有则返回false。
WithBaseObject() | 如果此环境记录与**with**语句关联，则返回with宾语。 否则，返回undefined。
