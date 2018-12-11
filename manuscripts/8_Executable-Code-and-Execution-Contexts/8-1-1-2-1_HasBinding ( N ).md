# 8.1.1.1.1 HasBinding ( N )

The concrete Environment Record method HasBinding for object Environment Records determines if its associated binding object has a property whose name is the value of the argument N:

1. Let *envRec* be the object Environment Record for which the method was invoked.
2. Let *bindings* be the binding object for *envRec*.
3. Let *foundBinding* be ? HasProperty(*bindings*, N).
4. If *foundBinding* is false, return false.
5. If the *withEnvironment* flag of *envRec* is false, return true.
6. Let *unscopables* be ? Get(*bindings*, @@unscopables).
7. If Type(*unscopables*) is Object, then
      a. Let *blocked* be ToBoolean(? Get(*unscopables*, N)).
      b. If *blocked* is true, return false.
8. Return true.

对象式环境记录的具体环境记录方法HasBinding，确定其关联的绑定对象是否具有名称为参数N的值的属性：

1.令*envRec*成为调用该方法的对象式环境记录项。
2.让* bindings *成为* envRec *的绑定对象。
3.让* foundBinding *成为？ HasProperty（* bindings *，N）。
4.如果* foundBinding *为false，则返回false。
5.如果* envRec *的* withEnvironment *标志为false，则返回true。
6.让* unscopables *成为？ 获取（* bindings *，@@ unscopables）。
7.如果Type（* unscopables *）是Object，那么
       一个。 设*阻止*为ToBoolean（？Get（* unscopables *，N））。
      湾 如果* blocked *为true，则返回false。
8.返回true。