# 8.1.1.1.1 HasBinding ( N )

The concrete Environment Record method HasBinding for declarative Environment Records simply determines if the argument identifier is one of the identifiers bound by the record:

1. Let *envRec* be the declarative Environment Record for which the method was invoked.
2. If *envRec* has a binding for the name that is the value of N, return true.
3. Return false.