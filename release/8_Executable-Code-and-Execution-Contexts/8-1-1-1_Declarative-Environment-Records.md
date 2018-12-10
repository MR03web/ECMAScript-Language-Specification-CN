# 8.1.1.1 Declarative Environment Records 声明式环境记录项

Each declarative Environment Record is associated with an ECMAScript program scope containing variable, constant, let, class, module, import, and/or function declarations. A declarative Environment Record binds the set of identifiers defined by the declarations contained within its scope.

每个声明式环境记录项都与一个ECMAScript程序作用域相管理，该作用域包含variable、constant、let、class、module、import和（或）函数声明。声明式环境记录项用于绑定作用域内声明定义的标识符。

The behaviour of the concrete specification methods for declarative Environment Records is defined by the following algorithms.

声明式环境记录的具体规范方法的行为由以下算法定义。