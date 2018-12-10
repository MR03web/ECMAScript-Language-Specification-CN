# 8.1.1.1.6 GetBindingValue ( N, S )

The concrete Environment Record method GetBindingValue for declarative Environment Records simply returns the value of its bound identifier whose name is the value of the argument N. If the binding exists but is uninitialized a **ReferenceError** is thrown, regardless of the value of S.

1. Let *envRec* be the declarative Environment Record for which the method was invoked.
2. Assert: *envRec* has a binding for N.
3. If the binding for N in envRec is an uninitialized binding, throw a ReferenceError exception.
4. Return the value currently bound to N in *envRec*.

声明式环境记录的具体环境记录方法GetBindingValue，返回其绑定标识符的值，其名称是参数N的值。如果绑定存在但未初始化，则抛出**ReferenceError**，而不管S的值如何。

1. 设*envRec*是调用该方法时的声明式环境记录。
2. 断言：*envRec*具有绑定N。
3. 如果envRec中绑定N是未初始化的绑定，则抛出ReferenceError异常。
4. 在*envRec*中返回当前绑定到N的值。