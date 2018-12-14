# 8.1.1.1.5 SetMutableBinding ( N, V, S )

The concrete Environment Record method SetMutableBinding for object Environment Records attempts to set the value of the Environment Record's associated binding object's property whose name is the value of the argument N to the value of argument V. A property named N normally already exists but if it does not or is not currently writable, error handling is determined by the value of the Boolean argument S.

1. Let *envRec* be the object Environment Record for which the method was invoked.
2. Let *bindings* be the binding object for *envRec*.
3. Return ? Set(bindings, N, V, S).

对象式环境记录的具体环境记录方法SetMutableBinding，尝试设置环境记录的关联绑定对象属性N的值为V。名为N的属性通常已经存在，如果它不存在或属性不可写，错误处理由布尔参数S的值确定。

1.令*envRec*成为调用该方法的对象式环境记录项。
2.让*bindings*成为*envRec*的绑定对象。
3.返回 ？ Set（*bindings*，N，V，S）。