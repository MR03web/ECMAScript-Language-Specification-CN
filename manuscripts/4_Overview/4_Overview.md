# 4 Overview 概述

This section contains a non-normative overview of the ECMAScript language.

本章节包含对ECMAScript语言非规范性的概述。

ECMAScript is an object-oriented programming language for performing computations and manipulating computational objects within a host environment. ECMAScript as defined here is not intended to be computationally self-sufficient; indeed, there are no provisions in this specification for input of external data or output of computed results. Instead, it is expected that the computational environment of an ECMAScript program will provide not only the objects and other facilities described in this specification but also certain environment-specific objects, whose description and behaviour are beyond the scope of this specification except to indicate that they may provide certain properties that can be accessed and certain functions that can be called from an ECMAScript program.

ECMAScript是一种面向对象编程语言，在宿主环境中执行计算和操作计算对象。这里定义的ECMAScript并未打算要计算性自足；事实上，本规范没有对于外部数据输入或计算结果输出的规定。相反，我们期望ECMAScript程序的计算环境不但提供本规范中描述的对象和特性，还提供一些环境特有的对象，除了说明可被ECMAScript程序访问的属性和调用的方法外，这些对象的其它描述和行为超出了本规范的范围。

ECMAScript was originally designed to be used as a scripting language, but has become widely used as a general-purpose programming language. A scripting language is a programming language that is used to manipulate, customize, and automate the facilities of an existing system. In such systems, useful functionality is already available through a user interface, and the scripting language is a mechanism for exposing that functionality to program control. In this way, the existing system is said to provide a host environment of objects and facilities, which completes the capabilities of the scripting language. A scripting language is intended for use by both professional and non-professional programmers.