# 4.2 ECMAScript Overview ECMAScript概述

The following is an informal overview of ECMAScript—not all parts of the language are described. This overview is not part of the standard proper.

下面是ECMAScript非正式的概述 --- 并未描述语言的所有部分。此概述并非标准的组成部分。

ECMAScript is object-based: basic language and host facilities are provided by objects, and an ECMAScript program is a cluster of communicating objects. In ECMAScript, an *object* is a collection of zero or more *properties* each with *attributes* that determine how each property can be used—for example, when the Writable attribute for a property is set to false, any attempt by executed ECMAScript code to assign a different value to the property fails. Properties are containers that hold other objects, *primitive values*, or *functions*. A primitive value is a member of one of the following built-in types: **Undefined**, **Null**, **Boolean**, **Number**, **String**, and **Symbol**; an object is a member of the built-in type **Object**; and a function is a callable object. A function that is associated with an object via a property is called a *method*.

ECMAScript是基于对象的：基本语言和宿主机能都由对象提供，ECMAScript程序是相互通信的对象的集群。在ECMAScript中，一个*对象*是零个或多个*属性*的集合，每个属性都有*特性*，它决定了这个属性怎样使用。例如，当设置一个属性的Writable特性为false时，任何试图修改这个属性值的ECMAScript代码的都会运行失败。属性是承载其它对象、*原始值*、*函数*的容器，原始值是以下内置类型之一：**Undefined**、**Null**、**Boolean**、**Number**、**String**和**Symbol**。对象是剩下的内置类型**Object**。函数是一个可调用对象。当一个函数通过属性和对象关联时，称其为*方法*。

ECMAScript defines a collection of *built-in objects* that round out the definition of ECMAScript entities. These built-in objects include the global object; objects that are fundamental to the runtime semantics of the language including **Object**, **Function**, **Boolean**, **Symbol**, and various **Error** objects; objects that represent and manipulate numeric values including **Math**, **Number**, and **Date**; the text processing objects **String** and **RegExp**; objects that are indexed collections of values including **Array** and nine different kinds of Typed Arrays whose elements all have a specific numeric data representation; keyed collections including **Map** and **Set** objects; objects supporting structured data including the **JSON** object, **ArrayBuffer**, **SharedArrayBuffer**, and **DataView**;

 objects supporting control abstractions including generator functions and **Promise objects**; and reflection objects including **Proxy** and **Reflect**.

ECMAScript定义了完整的ECMAScript实体的内置对象集合。这些内置对象包括全局对象；构成语言运行语言基础的对象包括**Object**、**Function**、**Boolean**、**Symbol**和各种**Error**对象；表示和操作数值的对象包括 **Math**, **Number**和**Date**；用于文本处理的对象**String**和**RegExp**；索引集合对象包括**Array**和9种不同类型的表示特定数值数据的限定类型数组[^1]；基于键的集合包括**Map**和**Set**；支持结构化数据的对象**JSON**、**ArrayBuffer**、**SharedArrayBuffer**、和**DataView**；支持控制抽象的generator函数和**Promise objects**对象；反射对象**Proxy**和**Reflect**。

ECMAScript also defines a set of built-in *operators*. ECMAScript operators include various unary operations, multiplicative operators, additive operators, bitwise shift operators, relational operators, equality operators, binary bitwise operators, binary logical operators, assignment operators, and the comma operator.

ECMAScript中还定义一组内置的*操作符*。ECMAScript运算符包括一元运算操作符、乘法操作符、加法操作符、位移操作符、关系操作符、相等操作符、二进制位操作符、二进制逻辑操作符、赋值操作符、逗号操作符。

Large ECMAScript programs are supported by *modules* which allow a program to be divided into multiple sequencesof statements and declarations. Each module explicitly identifies declarations it uses that need to be provided by othermodules and which of its declarations are available for use by other modules.

大型的ECMAScript程序支持模块化，即允许程序拆分成多个有关联的语句和声明的序列。每个模块都显式地标识它所使用的声明，该声明由其他模块提供，并且它的声明可供其他模块使用。

ECMAScript syntax intentionally resembles Java syntax. ECMAScript syntax is relaxed to enable it to serve as an easy-to-use scripting language. For example, a variable is not required to have its type declared nor are types associated with properties, and defined functions are not required to have their declarations appear textually before calls to them.

ECMAScript的语法有意设计成与Java语法类似。ECMAScript语法是松散的，这使其成为一个易于使用的脚本语言。例如，一个变量不需要有类型声明，属性也不需要与类型关联，定义的函数也不需要声明在函数调用词句的前面。

[^1]: [TypedArray对象](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/TypedArray)