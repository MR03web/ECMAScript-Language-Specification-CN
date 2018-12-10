# 8.1.1.1.5 SetMutableBinding ( N, V, S )

The concrete Environment Record method SetMutableBinding for declarative Environment Records attempts to change the bound value of the current binding of the identifier whose name is the value of the argument N to the value of argument V. A binding for N normally already exists, but in rare cases it may not. If the binding is an immutable binding, a **TypeError** is thrown if S is true.

1. Let *envRec* be the declarative Environment Record for which the method was invoked.
2. If *envRec* does not have a binding for N, then
      a. If S is true, throw a ReferenceError exception.
      b. Perform envRec.CreateMutableBinding(N, true).
      c. Perform envRec.InitializeBinding(N, V).
      d. Return NormalCompletion(empty).
3. If the binding for N in *envRec* is a strict binding, set S to true.
4. If the binding for N in *envRec* has not yet been initialized, throw a ReferenceError exception.
5. Else if the binding for N in *envRec* is a mutable binding, change its bound value to V.
6. Else,
      a. Assert: This is an attempt to change the value of an immutable binding.
      b. If S is true, throw a **TypeError** exception.
7. Return NormalCompletion(empty).

声明式环境记录的具体环境记录方法SetMutableBinding，尝试将名称为参数N的值的当前绑定的绑定值更改为参数V的值。绑定N通常已经存在，但在极少数情况下可能没有。如果绑定是不可变绑定，那么S为真时，会抛出**TypeError**。

1. 设*envRec*是调用该方法时的声明式环境记录。
2. 如果*envRec*没有绑定N，那么
      a. 如果S为true，则抛出ReferenceError异常。
      b. 执行envRec.CreateMutableBinding（N，true）。
      c. 执行envRec.InitializeBinding（N，V）。
      d. 返回NormalCompletion（空）。
3. 如果*envRec*中N的绑定是严格绑定，则将S设置为true。
4. 如果尚未初始化*envRec*中N的绑定，则抛出ReferenceError异常。
5. 否则如果*envRec*中N的绑定是可变绑定，则将其绑定值更改为V。
6. 否则，
      a. 断言：这是尝试更改不可变绑定的值。
      b. 如果S为真，则抛出TypeError异常。
7. 返回NormalCompletion（空）。

> **NOTE** An example of ECMAScript code that results in a missing binding at step 2 is:
> function f(){eval("var x; x = (delete x, 0);")}
>
> **注意** 在步骤2中导致丢失绑定的ECMAScript代码的示例是：
> function f(){eval("var x; x = (delete x, 0);")}