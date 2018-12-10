# 8.1.1.1.3 CreateImmutableBinding ( N, S )

The concrete Environment Record method CreateImmutableBinding for declarative Environment Records creates a new immutable binding for the name N that is uninitialized. A binding must not already exist in this Environment Record for N. If the Boolean argument S has the value true the new binding is marked as a strict binding.

1. Let envRec be the declarative Environment Record for which the method was invoked.
2. Assert: envRec does not already have a binding for N.
3. Create an immutable binding in envRec for N and record that it is uninitialized. If S is true, record that the newly created binding is a strict binding.
4. Return NormalCompletion(empty).

声明式环境记录的具体环境记录方法CreateImmutableBinding，创建一个新的未初始化的不可变绑定N。此前环境记录中不得存在名称为N的绑定。如果布尔参数S的值为true，则新绑定将标记为严格绑定。

1. 设*envRec*是调用该方法时的声明式环境记录。
2. 断言：*envRec*没有绑定N。
3. 在*envRec*中为N创建一个不可变绑定，并记录它是未初始化的。
4. 返回NormalCompletion（空）。