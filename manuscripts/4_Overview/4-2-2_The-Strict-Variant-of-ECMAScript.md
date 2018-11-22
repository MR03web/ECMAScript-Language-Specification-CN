# 4.2.2 The Strict Variant of ECMAScript ECMAScript 严格模式变体

The ECMAScript Language recognizes the possibility that some users of the language may wish to restrict their usage of some features available in the language. They might do so in the interests of security, to avoid what they consider to be error-prone features, to get enhanced error checking, or for other reasons of their choosing. In support of this possibility, ECMAScript defines a strict variant of the language. The strict variant of the language excludes some specific syntactic and semantic features of the regular ECMAScript language and modifies the detailed semantics of some features. The strict variant also specifies additional error conditions that must be reported by throwing error exceptions in situations that are not specified as errors by the non-strict form of the language.

ECMAScript考虑到有些用户希望在使用时限制语言的一些特性的用法。他们这样做可能是为了安全考虑，避免一些他们认为容易出错的特性，获得增强的错误检查或其他原因。为了支持这种场景，ECMAScript定义了语言的一个严格变体。严格变体也定义了附加的错误情况，会通过抛出错误异常的方式来报告这些错误，而这些错误情况在语言非严格模式下并不认为是错误。

The strict variant of ECMAScript is commonly referred to as the *strict mode* of the language. Strict mode selection and use of the strict mode syntax and semantics of ECMAScript is explicitly made at the level of individual ECMAScript source text units. Because strict mode is selected at the level of a syntactic source text unit, strict mode only imposes restrictions that have local effect within such a source text unit.

Strict mode does not restrict or modify any aspect of the ECMAScript semantics that must operate consistently across multiple source text units. A complete ECMAScript program may be composed of both strict mode and non-strict mode ECMAScript source text units. In this case, strict mode only applies when actually executing code that is defined within a strict mode source text unit.

ECMAScript的严格变体通常被称为语言的*严格模式*。严格模式范围的确定和严格模式的语法和语义的使用，是在单个的ECMAScript源文本单元上进行明确指定。因为严格模式是在句法源文本单元上选择的，严格模式只在这个源文本单元上施加限制。严格模式不限制或修改ECMAScript语义的任何方面，以使多个代码文本单元保持一致的语义。一个ECMAScript程序可由严格模式和非严格模式的源代码单元组成。在这种情况下，严格模式只适用于定义了严格模式的代码单元内实际执行的代码。

In order to conform to this specification, an ECMAScript implementation must implement both the full unrestricted ECMAScript language and the strict variant of the ECMAScript language as defined by this specification. In addition, an implementation must support the combination of unrestricted and strict mode source text units into a single composite program.

为了符合此规范，ECMAScript的实现必须同时实现无限制的ECMAScript语言和本规范定义的ECMAScript的严格模式变体。此外，实现还必须支持无限制的和严格模式代码单元的在同一个程序中混用。