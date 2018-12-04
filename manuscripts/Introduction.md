# Introduction 介绍

This Ecma Standard defines the ECMAScript 2018 Language. It is the ninth edition of the ECMAScript Language Specification. Since publication of the first edition in 1997, ECMAScript has grown to be one of the world's most widely used general-purpose programming languages. It is best known as the language embedded in web browsers but has also been widely adopted for server and embedded applications.

该Ecma标准定义了ECMAScript 2018，这是ECMAScript语言的第九个版本[^1]。自1997年发布第一版以来，ECMAScript已发展为世界上使用最广泛的通用编程语言之一，它作为Web浏览器的内嵌语言而广为人知，但也被广泛用于服务器和嵌入式应用。

ECMAScript is based on several originating technologies, the most well-known being JavaScript (Netscape) and JScript (Microsoft). The language was invented by Brendan Eich at Netscape and first appeared in that company's Navigator 2.0 browser. It has appeared in all subsequent browsers from Netscape and in all browsers from Microsoft starting with Internet Explorer 3.0.

ECMAScript基于几种技术来源，最为著名的是JavaScript(Netscape[^2])和JScript(Microsoft)。这种语言是由Brendan Eich在Netscape发明，于该公司的Navigator 2.0浏览器之上首次出现。并在Netscape的所有后续浏览器和Microsoft的Internet Explorer 3.0及其之后的所有浏览器中一直出现。

The development of the ECMAScript Language Specification started in November 1996. The first edition of this Ecma Standard was adopted by the Ecma General Assembly of June 1997.

ECMAScript语言规范的开发始于1996年11月。1997年6月Ecma大会通过本标准的第一版。

That Ecma Standard was submitted to ISO/IEC JTC 1 for adoption under the fast-track procedure, and approved as international standard ISO/IEC 16262, in April 1998. The Ecma General Assembly of June 1998 approved the second edition of ECMA-262 to keep it fully aligned with ISO/IEC 16262. Changes between the first and the second edition are editorial in nature.

上述Ecma标准以快速通道程序[^3]提交给ISO / IEC JTC 1，并在1998年4月被批准为ISO/IEC 16262国际标准。Ecma大会在1998年6月通过了ECMA-262的第二版以保证其与ISO/IEC 16262完全一致。第一版和第二版之间只有编辑上的变动。

The third edition of the Standard introduced powerful regular expressions, better string handling, new control statements, try/catch exception handling, tighter definition of errors, formatting for numeric output and minor changes in anticipation of future language growth. The third edition of the ECMAScript standard was adopted by the Ecma General Assembly of December 1999 and published as ISO/IEC 16262:2002 in June 2002.

标准第三版引入了强大的正则表达式，更好的字符串处理，新的控制语句，try/catch异常处理，更严格的错误定义，格式化的数字输出以及一些为了未来语言的发展而预留的变动。1999年12月的Ecma大会通过了标准第三版，并在2002年6月作为ISO/IEC 16262:2002发布。

After publication of the third edition, ECMAScript achieved massive adoption in conjunction with the World Wide Web where it has become the programming language that is supported by essentially all web browsers. Significant work was done to develop a fourth edition of ECMAScript. However, that work was not completed and not published as the fourth edition of ECMAScript but some of it was incorporated into the development of the sixth edition.

自第三版发布以来，ECMAScript结合万维网获得了广泛应用，它实际上成为了所有web浏览器都支持的编程语言。为了编制ECMAScript第四版进行了很多有意义的工作，尽管这些工作没能完成且没有发布第四版，但是其中一些（特性或提案）纳入了第六版的开发中。

The fifth edition of ECMAScript (published as ECMA-262 5 th edition) codified de facto interpretations of the language specification that have become common among browser implementations and added support for new features that had emerged since the publication of the third edition. Such features include accessor properties, reflective creation and inspection of objects, program control of property attributes, additional array manipulation functions, support for the JSON object encoding format, and a strict mode that provides enhanced error checking and program security. The fifth edition was adopted by the Ecma General Assembly of December 2009.

ECMAScript第五版（发布为 ECMA-262 5 th edition）编纂了浏览器中已经普遍实现的事实语言规范，并且添加了从第三版以来就出现了的新功能的支持。这些功能包括访问器属性，反射创建和对象检测，属性特性的程序控制，新增的数组操作函数，JSON对象编码格式的支持，以及提供增强的错误检查和程序安全性的严格模式。该版本于2009年12月由Ecma大会通过。

The fifth edition was submitted to ISO/IEC JTC 1 for adoption under the fast-track procedure, and approved as Introduction Ecma International international standard ISO/IEC 16262:2011. Edition 5.1 of the ECMAScript Standard incorporated minor corrections and is the same text as ISO/IEC 16262:2011. The 5.1 Edition was adopted by the Ecma General Assembly of June 2011.

第五版按照快速通道程序提交ISO / IEC JTC 1，并通过为ISO / IEC 16262：2011国际标准。ECMAScript 5.1版包含了次要的修正和ISO / IEC 16262：2011的内容，5.1版由2011年6月的Ecma大会通过。

Focused development of the sixth edition started in 2009, as the fifth edition was being prepared for publication. However, this was preceded by significant experimentation and language enhancement design efforts dating to the publication of the third edition in 1999. In a very real sense, the completion of the sixth edition is the culmination of a fifteen year effort. The goals for this addition included providing better support for large applications, library creation, and for use of ECMAScript as a compilation target for other languages. Some of its major enhancements included modules, class declarations, lexical block scoping, iterators and generators, promises for asynchronous programming, destructuring patterns, and proper tail calls. The ECMAScript library of built-ins was expanded to support additional data abstractions including maps, sets, and arrays of binary numeric values as well as additional support for Unicode supplemental characters in strings and regular expressions. The built-ins were also made extensible via subclassing. The sixth edition provides the foundation for regular, incremental language and library enhancements. The sixth edition was adopted by the General Assembly of June 2015.

第六版的开发从2009年开始重点推进，因为第五版正在准备发布。但是，重要的实验和语言增强设计的努力可以追溯到1999年第三版发布前。确切来讲，第六版是集15年努力的大成之作。这个版本的目标是为大型应用程序、创建库、以及将ECMAScript作为其他语言的编译目标提供更好的支持。一些主要的增强包括：模块、类声明、词法块作用域，迭代器和生成器，异步编程的promises，解构模式，尾调用。ECMAScript内置库扩展了额外的数据抽象包括：maps，sets和二进制数组，以及对字符串和正则表达式中的Unicode补充字符的额外支持。内置库可以通过子类扩展。第六版提供正则、增量语言和库增强的基础。2015年6月，Ecma大会通过第六版。

ECMAScript 2016 was the first ECMAScript edition released under Ecma TC39's new yearly release cadence and open development process. A plain-text source document was built from the ECMAScript 2015 source document to serve as the base for further development entirely on GitHub. Over the year of this standard's development, hundreds of pull requests and issues were filed representing thousands of bug fixes, editorial fixes and other improvements. Additionally, numerous software tools were developed to aid in this effort including Ecmarkup, Ecmarkdown, and Grammarkdown. ES2016 also included support for a new exponentiation operator and adds a new method to Array.prototype called **includes**.

ECMAScript 2016是在Ecma TC39新的逐年发布和开放式开发流程下发布的第一个ECMAScript版本。在GitHub上，根据ECMAScript 2015源文档建立了一个纯文本源文档[^4]，以此做为未来开发的基础。在一年多的标准开发中，数以百计的pull requests和issues代表了数以千计的bug修复、编辑修复和其他改进。此外，还开发了许多软件工具来帮助完成这项工作，包括Ecmarkup，Ecmarkdown和Grammarkdown。ES2016还包括对新的幂操作符的支持，并为Array.prototype添加了一个名为**includes**的新方法。

This specification introduces Async Functions, Shared Memory, and Atomics along with smaller language and library enhancements, bug fixes, and editorial updates. Async functions improve the asynchronous programming experience by providing syntax for promise-returning functions. Shared Memory and Atomics introduce a new memory model that allows multi-agent programs to communicate using atomic operations that ensure a well-defined execution order even on parallel CPUs. This specification also includes new static methods on Object: **Object.values**, **Object.entries**, and **Object.getOwnPropertyDescriptors**.

此规范引入了异步函数、共享内存、原子操作[^5]、小的语言和库的增强、bug修复和编辑性更新。异步函数通过提供promise-returning函数语言来改进异步编程体验。共享内存和原子操作引入了一种新的内存模型，以允许多个代理程序使用原子操作进行通信，即使在并行CPU上也能确保明确定义的执行顺序。该规范还包括对象上的新静态方法：**Object.values**，**Object.entries**和**Object.getOwnPropertyDescriptors**。

Dozens of individuals representing many organizations have made very significant contributions within Ecma TC39 to the development of this edition and to the prior editions. In addition, a vibrant community has emerged supporting TC39's ECMAScript efforts. This community has reviewed numerous drafts, filed thousands of bug reports, performed implementation experiments, contributed test suites, and educated the world-wide developer community about ECMAScript. Unfortunately, it is impossible to identify and acknowledge every person and organization who has contributed to this effort.

代表各个组织的人们在Ecma TC39为本版本和之前版本的开发做出了非常重要的贡献。此外，一个充满活力的支持TC39 ECMAScript工作的社区已经出现。该社区已经审查了许多草案，提交了数千个bug报告，执行了实施实验，贡献了测试套件，并向全世界开发人员社区介绍了ECMAScript。遗憾的是，无法确认并感谢为此工作做出贡献的每个人和组织。

Allen Wirfs-Brock
ECMA-262, 6^th^ Edition Project Editor

Brian Terlson
ECMA-262, 7^th^ Edition Project Editor

Allen Wirfs-Brock
ECMA-262，第六版项目编辑

Brian Terlson
ECMA-262，第七版项目编辑

[^1]: [ECMAScript 历史版本](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Language_Resources)
[^2]: 网景通信公司
[^3]: [explanation-of-the-iso-fast-track-process](https://blogs.msdn.microsoft.com/brian_jones/2007/01/29/explanation-of-the-iso-fast-track-process)
[^4]: [Github上的ecma262](https://github.com/tc39/ecma262)
[^5]: [Atomics对象](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Atomics)