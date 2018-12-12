# 8.1.1.1.1 HasBinding ( N )

The concrete Environment Record method HasBinding for declarative Environment Records simply determines if the argument identifier is one of the identifiers bound by the record:

1. Let *envRec* be the declarative Environment Record for which the method was invoked.
2. If *envRec* has a binding for the name that is the value of N, return true.
3. Return false.

声明式环境记录的具体方法HasBinding，简单地判断参数标识符是否是记录绑定的标识符之一：

1. 令*envRec*成为调用该方法时的声明式环境记录。
2. 如果*envRec*有一个名称为N的绑定，返回true。
3. 如果没有该绑定，返回false。