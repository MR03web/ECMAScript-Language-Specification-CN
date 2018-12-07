# 8.1.1.1.7 DeleteBinding ( N )

The concrete Environment Record method DeleteBinding for declarative Environment Records can only delete bindings that have been explicitly designated as being subject to deletion.

1. Let *envRec* be the declarative Environment Record for which the method was invoked.
2. Assert: *envRec* has a binding for the name that is the value of N.
3. If the binding for N in *envRec* cannot be deleted, return false.
4. Remove the binding for N from *envRec*.
5. Return true.

声明性环境记录的实际环境记录方法DeleteBinding，只能删除已明确指定为可删除的绑定。

1. 设*envRec*是调用该方法时的声明性环境记录。
2. 断言：*envRec*具有绑定N。
3. 如果无法删除*envRec*中N的绑定，则返回false。
4. 从*envRec*中删除绑定N。
5. 返回true。
