# 2 Conformance 一致性

A conforming implementation of ECMAScript must provide and support all the types, values, objects, properties, functions, and program syntax and semantics described in this specification.

符合ECMAScript规范的实现，必须提供和支持规范中描述的所有类型，值，对象，属性，函数，程序语法和语义。

A conforming implementation of ECMAScript must interpret source text input in conformance with the latest version of the Unicode Standard and ISO/IEC 10646.

符合ECMAScript规范的实现，必须按照最新版的Unicode规范和ISO/IEC 10646来解释输入的源代码文本。

A conforming implementation of ECMAScript that provides an application programming interface (API) that supports programs that need to adapt to the linguistic and cultural conventions used by different human languages and countries must implement the interface defined by the most recent edition of ECMA-402 that is compatible with this specification.

符合ECMAScript规范的实现，提供了一个应用程序接口(API)，以支持需要适应不同人类语言和国家的语言和文化传统的程序，必须实现兼容本规范的最新版ECMA-402[^1]定义的接口。

A conforming implementation of ECMAScript may provide additional types, values, objects, properties, and functions beyond those described in this specification. In particular, a conforming implementation of ECMAScript may provide properties not described in this specification, and values for those properties, for objects that are described in this specification.

符合ECMAScript规范的实现，可以额外支持超出本规范描述的类型，值，对象，属性和函数，另外，符合规范的实现可以为本规范中描述的对象提供额外的属性和属性的值。

A conforming implementation of ECMAScript may support program and regular expression syntax not described in this specification. In particular, a conforming implementation of ECMAScript may support program syntax that makes use of the “future reserved words” listed in subclause 11.6.2.2 of this specification.

符合ECMAScript规范的实现，可以支持超出规范描述的程序和正则表达式语法，另外，符合规范的实现可以使用11.6.2.2 节所列出的“未来保留字”做为程序语法。

A conforming implementation of ECMAScript must not implement any extension that is listed as a Forbidden Extension in subclause 16.2.

符合ECMAScript规范的实现，禁止实现16.2节中列举的禁用扩展。

[^1]: [Ecma-402](http://www.ecma-international.org/publications/standards/Ecma-402.htm)
