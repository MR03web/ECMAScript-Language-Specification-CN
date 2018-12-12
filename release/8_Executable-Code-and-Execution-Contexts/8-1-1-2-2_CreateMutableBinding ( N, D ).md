# 8.1.1.1.2 CreateMutableBinding ( N, D )

The concrete Environment Record method CreateMutableBinding for object Environment Records creates in an Environment Record's associated binding object a property whose name is the String value and initializes it to the value undefined. If Boolean argument D has the value true the new property's `[[Configurable]]` attribute is set to true;otherwise it is set to false.

1. Let *envRec* be the object Environment Record for which the method was invoked.
2. Let *bindings* be the binding object for *envRec*.
3. Return ? DefinePropertyOrThrow(*bindings*, N, PropertyDescriptor { `[[Value]]`: undefined, `[[Writable]]`: true, `[[Enumerable]]`: true, `[[Configurable]]`: D }).

> **NOTE** Normally *envRec* will not have a binding for N but if it does, the semantics of DefinePropertyOrThrow may result in an existing binding being replaced or shadowed or cause an abrupt completion to be returned.

对象环境记录的具体方法CreateMutableBinding，在环境记录的关联绑定对象中创建一个名称为String值的属性，并将其初始化为undefined值。如果Boolean参数D的值为true，则新属性的`[[Configurable]]`属性设置为true；否则设置为false。

1.令*envRec*成为调用该方法的对象式环境记录项。
2.令*bindings*成为*envRec*的绑定对象。
3.返回 ？ DefinePropertyOrThrow（*bindings*，N，PropertyDescriptor {`[[Value]]`：undefined，`[[Writable]]`：true，`[[Enumerable]]`：true，`[[Configurable]]`：D}）。