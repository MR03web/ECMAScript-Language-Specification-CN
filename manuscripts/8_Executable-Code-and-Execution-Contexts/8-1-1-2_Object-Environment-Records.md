# 8.1.1.2 Object Environment Records 对象式环境记录项

Each object Environment Record is associated with an object called its *binding object*. An object Environment Record binds the set of string identifier names that directly correspond to the property names of its binding object. Property keys that are not strings in the form of an *IdentifierName* are not included in the set of bound identifiers. Both own and inherited properties are included in the set regardless of the setting of their `[[Enumerable]]` attribute. Because properties can be dynamically added and deleted from objects, the set of identifiers bound by an object Environment Record may potentially change as a side-effect of any operation that adds or deletes properties. Any bindings that are created as a result of such a side-effect are considered to be a mutable binding even if the Writable attribute of the corresponding property has the value false. Immutable bindings do not exist for object Environment Records.

每个对象式环境记录都与一个名为*绑定对象*的对象相关联。对象式环境记录项将一系列标识符和对应绑定对象的属性名称建立对应关系。不符合*IdentifierName*不会作为绑定的标识符使用。无论该属性的`[[Enumerable]]`特性是什么，对象自身和继承的属性都会作为绑定。由于可以从对象动态添加和删除属性，因此对象式环境记录项所绑定的标识符集合也会隐匿地变化，这是增减绑定对象的属性而产生的副作用。由于这种副作用而创建的任何绑定都被认为是可变绑定，即使相应属性的Writable属性值为false也是如此。对象环境记录不存在不可变绑定。

Object Environment Records created for **with** statements (13.11) can provide their binding object as an implicit **this** value for use in function calls. The capability is controlled by a withEnvironment Boolean value that is associated with each object Environment Record. By default, the value of withEnvironment is false for any object Environment Record.

对象式环境记录项可以通过配置的方式，将其绑定对象合为函数调用时的隐式this 对象的值。这一功能用于规范 With 表达式（13.11章）引入的绑定行为。该行为通过对象式环境记录项中Boolean类型的withEnvironment控制，默认情况下，withEnvironment的值为 false。

The behaviour of the concrete specification methods for object Environment Records is defined by the following algorithms.

对象式环境记录的具体规范方法的行为由以下算法定义。