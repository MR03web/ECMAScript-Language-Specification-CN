# 8.1.1.1.4 InitializeBinding ( N, V )

The concrete Environment Record method InitializeBinding for declarative Environment Records is used to set the bound value of the current binding of the identifier whose name is the value of the argument N to the value of argument V. An uninitialized binding for N must already exist.

1. Let *envRec* be the declarative Environment Record for which the method was invoked.
2. Assert: *envRec* must have an uninitialized binding for N.
3. Set the bound value for N in *envRec* to V.
4. Record that the binding for N in *envRec* has been initialized.
5. Return NormalCompletion(empty).

声明性环境记录的实际环境记录方法InitializeBinding，用于将名称为N的当前绑定的绑定值设置为参数V的值。此前环境记录中须存在名称为N的未初始化绑定。

1. 设*envRec*是调用该方法时的声明性环境记录。
2. 断言：*envRec*具有N的未初始化绑定。
3. 将*envRec*中N的绑定值设置为V.
4. 记录*envRec*中N的绑定已初始化。
5. 返回NormalCompletion（空）。