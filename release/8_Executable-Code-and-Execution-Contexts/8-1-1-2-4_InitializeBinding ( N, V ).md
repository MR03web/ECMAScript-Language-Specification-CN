# 8.1.1.1.4 InitializeBinding ( N, V )

The concrete Environment Record method InitializeBinding for object Environment Records is used to set the bound value of the current binding of the identifier whose name is the value of the argument N to the value of argument V. An uninitialized binding for N must already exist.

1. Let *envRec* be the object Environment Record for which the method was invoked.
2. Assert: *envRec* must have an uninitialized binding for N.
3. Record that the binding for N in *envRec* has been initialized.
4. Return ? *envRec*.SetMutableBinding(N, V, false).

> **NOTE** In this specification, all uses of CreateMutableBinding for object Environment Records are immediately followed by a call to InitializeBinding for the same name. Hence, implementations do not need to explicitly track the initialization state of individual object Environment Record bindings.

对象式环境记录的具体方法InitializeBinding，用于将当前绑定N的绑定值设置为参数V。未初始化绑定N必须已存在。

1.令*envRec*成为调用该方法的对象式环境记录项。
2.断言：*envRec*必须具有未初始化绑定N。
3.记录*envRec*中N的绑定为已初始化。
4.返回 ？*envRec*.SetMutableBinding（N，V，false）。

> **注意** 在本规范中，所有对象式环境记录的CreateMutableBinding方法的使用，紧接着是对同一个N的InitializeBinding的调用。因此，实现不需要显式跟踪单个对象式环境记录绑定的初始化状态。