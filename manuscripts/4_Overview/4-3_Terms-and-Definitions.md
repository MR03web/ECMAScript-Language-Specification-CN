# 4.3 Terms and Definitions 术语和定义

For the purposes of this document, the following terms and definitions apply.

本文档将使用下列术语和定义。

## 4.3.1 type 类型

set of data values as defined in clause 6 of this specification

第6章定义数据的集合

## 4.3.2 primitive value 原始值

member of one of the types Undefined, Null, Boolean, Number, Symbol, or String as defined in clause 6

第6章中定义的Undefined、Null、Boolean、Number、Symbol或String类型之一

> **NOTE** A primitive value is a datum that is represented directly at the lowest level of the language implementation.
>
> **注意** 原始值直接代表语言实现的最底层的数据。

## 4.3.3 object 对象

member of the type Object

Object类型的成员

> **NOTE** An object is a collection of properties and has a single prototype object. The prototype may be the null value.
>
> **NOTE** 对象是属性的集合，并有一个唯一的原型对象。原型可以是null值。

## 4.3.4 constructor 构造器

function object that creates and initializes objects

创建和初始化对象的函数对象

> **NOTE** The value of a constructor's **prototype** property is a prototype object that is used to implement inheritance and shared properties.
>
> **注意** 构造器的**prototype**属性是一个prototype对象，用来实现继承和共享属性。

## 4.3.5 prototype 原型对象

object that provides shared properties for other

为其他对象提供共享属性的对象

> **NOTE** When a constructor creates an object, that object implicitly references the constructor's **prototype** property for the purpose of resolving property references. The constructor's **prototype** property can be referenced by the program expression `constructor.prototype`, and properties added to an object's prototype are shared, through inheritance, by all objects sharing the prototype. Alternatively, a new object may be created with an explicitly specified prototype by using the `Object.create` built-in function.
>
> **注意** 当构造函数创建一个对象时，为了解决对象的属性引用，该对象会隐式引用构造函数的**prototype**属性。通过程序表达式`constructor.prototype`可以引用到构造器的**prototype**属性，同时添加到对象的prototype上的属性，通过继承，会被有同一个prototype的所有对象共享。另外，可以使用内置函数`Object.create` ，通过显示指定原型来创建一个新对象。

## 4.3.6 ordinary object 普通对象

object that has the default behaviour for the essential internal methods that must be supported by all objects

具有所有对象必须支持的基本内部方法的默认行为的对象

## 4.3.7 exotic object 奇异对象

object that does not have the default behaviour for one or more of the essential internal methods

对于一个或多个基本内部方法没有默认行为的对象

> **NOTE** Any object that is not an ordinary object is an exotic object.
>
> **注意** 任何对象不是普通对象就是奇异对象。

## 4.3.8 standard object 标准对象

object whose semantics are defined by this specification

由本规范定义语义的对象

## 4.3.9 built-in object 内置对象

object specified and supplied by an ECMAScript implementation

由ECMAScript实现指定和提供的对象

> **NOTE** Standard built-in objects are defined in this specification. An ECMAScript implementation may specify and supply additional kinds of built-in objects. A built-in constructor is a built-in object that is also a constructor.
>
> **注意** 标准内置对象由此规范定义。一个ECMAScript实现可以指定和提供其他类型的内置对象。一个内置的构造器是一个内置对象，也是一个构造器。

## 4.3.10 undefined value 未定义值

primitive value used when a variable has not been assigned a value

未赋值变量的原始值

## 4.3.11 Undefined type 未定义类型

type whose sole value is the **undefined** value

一个类型，它的唯一值是**undefined**

## 4.3.12 null value 空值

primitive value that represents the intentional absence of any object value

一个原始值，用来表示对象的缺省值的原始值

## 4.3.13 Null type 空类型

type whose sole value is the null value

一个类型，它的唯一值是**null**

## 4.3.14 Boolean value 布尔值

member of the Boolean type

布尔类型的成员。

> **NOTE** There are only two Boolean values, **true** and **false**.
>
> **注意** 只有两个布尔值，**true**和**false**。

## 4.3.15 Boolean type 布尔类型

type consisting of the primitive values **true** and **false**

由原始值**true**和**false**组成的类型

## 4.3.16 Boolean object 布尔对象

member of the Object type that is an instance of the standard built-in **Boolean** constructor

对象类型的成员，它是标准内置构造器**Boolean**的一个实例

> **NOTE** A Boolean object is created by using the **Boolean** constructor in a **new** expression, supplying a Boolean value as an argument. The resulting object has an internal slot whose value is the Boolean value. A Boolean object can be coerced to a Boolean value.
>
> **注意** 通过**new**表达式使用**Boolean**构造器创建一个布尔对象，支持一个布尔值作为参数。生成的对象有一个内部slot，它的值是布尔值。一个布尔对象可以强制转换为一个布尔值。

## 4.3.17 String value 字符串值

primitive value that is a finite ordered sequence of zero or more 16-bit unsigned integer values

原始值，它是零个或多个16位无符号整数组成的有限有序序列。

> **NOTE** A String value is a member of the String type. Each integer value in the sequence usually represents a single 16-bit unit of UTF-16 text. However, ECMAScript does not place any restrictions or requirements on the values except that they must be 16-bit unsigned integers.
>
> **注意** 字符串值是字符串类型的成员。序列中的每个整数值通常表示UTF-16文本的单个16位单元。然而，对于其值，ECMAScript只要求必须是16位无符号整数，除此之外没有任何限制或要求。

## 字符串类型 (String type)

set of all possible String values

所有可能的字符串值的集合。

## 4.3.19 String object 字符串对象

member of the Object type that is an instance of the standard built-in **String** constructor

对象类型的成员，它是标准内置构造器**String**的一个实例

> **NOTE** A String object is created by using the **String** constructor in a **new** expression, supplying a String value as an argument. The resulting object has an internal slot whose value is the String value. A String object can be coerced to a String value by calling the **String** constructor as a function (21.1.1.1).
>
> **注意** 通过**new**表达式使用**String**构造器创建一个字符串对象，支持一个字符串值作为参数。生成的对象有一个内部slot，其值是字符串值。通过将**String**构造器作为函数调用（21.1.1.1），可以将字符串对象强制为一个字符串值。

## 4.3.20 number value 数字值

primitive value corresponding to a double-precision 64-bit binary format IEEE 754-2008 value

原始值，对应一个64位双精度二进制IEEE 754-2008值

> **NOTE** A Number value is a member of the Number type and is a direct representation of a number.
>
> **注意** 数值是数值类型的一员，直接代表一个数字。

## 4.3.21 number type 数字类型

set of all possible Number values including the special “Not-a-Number” (NaN) value, positive infinity, and negative infinity

所有可能的数字值的集合，包括特殊的“Not-a-Number”(NaN) 值、正无穷、负无穷。

## 4.3.22 Number object 数字对象

member of the Object type that is an instance of the standard built-in **Number** constructor

对象类型的成员，它是标准内置构造器**Number**的一个实例

> **NOTE** A Number object is created by using the **Number** constructor in a **new** expression, supplying a number value as an argument. The resulting object has an internal slot whose value is the number value. A Number object can be coerced to a number value by calling the **Number** constructor as a function (20.1.1.1).
>
> **注意** 通过**new**表达式使用**Number**构造器创建一个数字对象，支持一个数字值作为参数。生成的对象有一个内部slot，其值是数字值。将**Number**构造器作为函数调用，可以将数字对象强制为数字值（20.1.1.1）。

## 4.3.23 Infinity 无穷大

number value that is the positive infinite number value

正无穷数字值

## 4.3.24 NaN Not-a-Number

number value that is an IEEE 754-2008 “Not-a-Number” value

值为IEEE 754-2008的“Not-a-Number”的数字值

## 4.3.25 Symbol value 符号值

primitive value that represents a unique, non-String Object property key

原始值，表示唯一的、非字符串的对象属性的key

## 4.3.26 Symbol type 符号类型

set of all possible Symbol values

所有可能的符号值的集合

## 4.3.27 Symbol object 符号对象

member of the Object type that is an instance of the standard built-in **Symbol** constructor

对象类型的成员，它是标准内置构造器**Symbol**的一个实例

## 4.3.28 function 函数

member of the Object type that may be invoked as a subroutine

对象类型的成员，它是标准内置构造器**Function**的一个实例，可以做为子程序被调用

> **NOTE** In addition to its properties, a function contains executable code and state that determine how it behaves when invoked. A function's code may or may not be written in ECMAScript.
>
> **注意** 函数除了它的属性外，还包含可执行代码和状态，用来确定它被调用时的行为。函数的代码不一定会被写入ECMAScript中。

## 4.3.29 build-in fucntion 内建函数

built-in object that is a function

作为函数的内置对象

> **NOTE** Examples of built-in functions include `parseInt` and `Math.exp`. An implementation may provide implementation-dependent built-in functions that are not described in this specification.
>
> **注意** 内置函数例如 `parseInt` 和 `Math.exp`。一个实现可以提供本规范没有描述的依赖于实现的内置函数。

## 4.3.30 property 属性

part of an object that associates a key (either a String value or a Symbol value) and a value

把对象的key（可以是字符串值或符号值）和value关联起来的部分

> **NOTE** Depending upon the form of the property the value may be represented either directly as a data value (a primitive value, an object, or a function object) or indirectly by a pair of accessor functions.
>
> **注意** 属性可能根据属性值的不同，可以直接表示为数据值（原始值、对象或函数），也可以由一对访问器函数间接表示。

## 4.3.31 method 方法

function that is the value of a property

做为属性值的函数

> **NOTE** When a function is called as a method of an object, the object is passed to the function as its this value.
>
> **注意** 当一个函数作为一个对象的方法被调用时，该对象将作为函数的`this`值传递给该函数。

## 4.3.32 build-in method 内建方法

method that is a built-in function

作为内置函数的方法

> **NOTE** Standard built-in methods are defined in this specification, and an ECMAScript implementation may specify and provide other additional built-in methods.
>
> **注意** 本规范中已经定了标准内置方法，ECMAScript的实现可以指定并提供额外的内置方法。

## 4.3.33 attribute 特性

internal value that defines some characteristic of a property

定义一个属性的一些特性的内部值

## 4.3.34 own property 自身属性

property that is directly contained by its object

对象直接拥有的属性

## 4.3.35 inherited property 继承属性

property of an object that is not an own property but is a property (either own or inherited) of the object's prototype

不是对象自身拥有的属性，而是对象原型的属性（原型的自身属性或继承属性）