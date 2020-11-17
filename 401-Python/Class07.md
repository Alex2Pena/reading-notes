#Understanding Scope

**Global scope**: The names that you define in this scope are available to all your code.

**Local scope**: The names that you define in this scope are only available or visible to the code within the scope.

**Namespaces**: These dictionaries are the concrete mechanisms that Python uses to store names. They’re stored in a special attribute called: ```__dict__```

**Local *(or function)* scope** is the code block or body of any Python function or lambda expression.

**Enclosing *(or nonlocal)* scope** is a special scope that only exists for nested functions. 

**Global *(or module)* scope** is the top-most scope in a Python program, script, or module.

**Built-in scope** is a special Python scope that’s created or loaded whenever you run a script or open an interactive session.

