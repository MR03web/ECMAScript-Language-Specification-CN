# 4 Overview 概述

This section contains a non-normative overview of the ECMAScript language.

本章节包含一个对ECMAScript语言的非规范性概述。

ECMAScript is an object-oriented programming language for performing computations and manipulating computational objects within a host environment. ECMAScript as defined here is not intended to be computationally self-sufficient; indeed, there are no provisions in this specification for input of external data or output of computed results. Instead, it is expected that the computational environment of an ECMAScript program will provide not only the objects and other facilities described in this specification but also certain environment-specific objects, whose description and behaviour are beyond the scope of this specification except to indicate that they may provide certain properties that can be accessed and certain functions that can be called from an ECMAScript program.

ECMAScript是一种面向对象编程语言，在宿主环境中执行计算和操作计算对象。这里定义的ECMAScript并未打算要计算性自足；事实上，本规范没有对于外部数据输入或计算结果输出的规定。相反，我们期望ECMAScript程序的计算环境不但提供本规范中描述的对象和机能，还提供一些环境特有的对象，除了说明可被ECMAScript程序访问的属性和调用的方法外，这些对象的其它描述和行为超出了本规范的范围。

ECMAScript was originally designed to be used as a scripting language, but has become widely used as a general-purpose programming language. A scripting language is a programming language that is used to manipulate, customize, and automate the facilities of an existing system. In such systems, useful functionality is already available through a user interface, and the scripting language is a mechanism for exposing that functionality to program control. In this way, the existing system is said to provide a host environment of objects and facilities, which completes the capabilities of the scripting language. A scripting language is intended for use by both professional and non-professional programmers.

ECMAScript最初被设计为一种脚本语言，但是已广泛用作通用编程语言。脚本语言是一种用于操作、自定义和自动化现有系统的编程语言。在这样的系统中，可用对象和机能已经可以通过用户接口使用，脚本语言是将这些功能暴露给程序控制的机制。通过这种方式，现有的系统可以说为补全脚本语言需要的对象和特性提供了一个宿主环境。脚本语言旨在提供给专业和非专业程序员使用。

ECMAScript was originally designed to be a Web scripting language, providing a mechanism to enliven Web pages in browsers and to perform server computation as part of a Web-based client-server architecture. ECMAScript is now used to provide core scripting capabilities for a variety of host environments. Therefore the core language is specified in this document apart from any particular host environment.

ECMAScript最初被设计成一种Web脚本语言，提供了一种使浏览器中的web页面活跃起来，并做为基于web的客户端-服务器体系结构的一部分执行服务器计算的机制。现在ECMAScript用于为各种宿主环境提供核心脚本功能。因此本文档是为不依赖特定宿主环境的语言核心部分做出规范。

ECMAScript usage has moved beyond simple scripting and it is now used for the full spectrum of programming tasks in many different environments and scales. As the usage of ECMAScript has expanded, so has the features and facilities it provides. ECMAScript is now a fully featured general-purpose programming language.

ECMAScript的使用已经超越了简单的脚本，它现在可用于许多不同环境和规模的全方位编程任务。随着ECMAScript的使用范围的扩大，它提供的功能和机能也在不断扩展。 ECMAScript现在是一种功能齐全的通用编程语言。

Some of the facilities of ECMAScript are similar to those used in other programming languages; in particular C, Java™, Self, and Scheme as described in:

ECMAScript的一些机能和其他编程语言的类似；特别是 Java™，Self，和Scheme。以下文献描述了他们：

Gosling, James, Bill Joy and Guy Steele. The Java™ Language Specification. Addison Wesley Publishing Co., 1996.

Ungar, David, and Smith, Randall B. Self: The Power of Simplicity. OOPSLA'87 Conference Proceedings, pp. 227–241, Orlando, FL, October 1987.

IEEE Standard for the Scheme Programming Language. IEEE Std 1178-1990.