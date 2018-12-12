# 8.1.1.1.2 CreateMutableBinding ( N, D )

The concrete Environment Record method CreateMutableBinding for declarative Environment Records creates a new mutable binding for the name N that is uninitialized. A binding must not already exist in this Environment Record for N. If Boolean argument D has the value true the new binding is marked as being subject to deletion.

1. Let *envRec* be the declarative Environment Record for which the method was invoked.
2. Assert: *envRec* does not already have a binding for N.
3. Create a mutable binding in *envRec* for N and record that it is uninitialized. If D is true, record that the newly created binding may be deleted by a subsequent DeleteBinding call.
4. Return NormalCompletion(empty).

声明式环境记录的具体方法CreateMutableBinding，会创建一个新的对于未初始化的名称N的可变绑定。此前环境记录中不得存在
名称为N的绑定。如果布尔参数D的值为true，则新绑定将标记为可删除。

1.令*envRec*成为调用该方法时的声明式环境记录。
2.断言：*envRec*没有绑定N。
3.在*envRec*中为N创建一个可变绑定，并记录它是未初始化的。 如果D为true，则记录可在后续操作中调用DeleteBinding删除新创建的绑定。
4.返回NormalCompletion（空）。