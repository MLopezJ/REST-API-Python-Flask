## Keywords 
Are reserved words in Python and are used to define the syntax and structure of the lenguage. They cant be used as var name, fuction name or any other identifier. There are 33 keywords in Python 3.7 but the number can change deppending of ther versions and in the course of the time. Must of the keywords are in lowercase except True, False, None. 

## Indentifiers  
Are names given to entities like class, functions, vars, etc. It helps to differentiate one entitie from another and can be a combination of letters in lowercase or uppercase or digits or an underscore but cant start with a digit and cant use special symbols. The indentifiers are case-sensitive.

## Statements 
Are instructions that the Python interpreter can execute, for example: asignations, conditionals, loops, etc. 

## Identation
Blocks of code are defined by identation

## Comments 
One line comments are written with # and multi-line comments with ''' or """

## Docstring
Docstring is short for documentation string. Are comments who are used to describe what a function, class, module or method does. They need to be as the first statement and are declared with triple quotes.

## Vars
Are location used to store data in memory. When a value is asign to a var, Python save the value in memory and assign the memory reference of the value to the var.

## Constants
Are data containers wich their values cant be changes. Are usually declared and assigned on a module.

## lowerCammelCase
Its the standard for name the vars and constants. 

## Data types
Every value in Python has a datatype. We dont have to forget that everything is an object in Python, so data types are actually classes and vars are instances (objects) of these classes.

    Numbers: int, float, complex
    Strings: Sequence on unicode chatacters
    List: ordered sequence of items. All the items in a list dont need to be the same type
    Tuple: Are ordered sequence of items too but they cant be modifies once created
    Set: Unordered collection of unique items. 
    Dictionary: unordered collection of key-value pairs
    Boolean: Logic value, could be True or False

## Type conversion
There is two ways to make type conversions:

    Implicit: The python interpreter automatically converts one data type to another. For example, when you make a sum between an int and a float, the result will be float.

    Explicit: Its made by the using of fuctions like int(), float(), str(), etc

## Names 
Everything in Python is an object, so, a Name is a indentifier for the objects. For example, in:
```Python
a = 2
```
2 will be stored in memory and 'a' will be the name associate with. 'a' and 2 will have the same RAM address. But even, if we make the following assignation:
```Python
b = 2
```
'a' and 'b' will have the same RAM address, becasue the value (2) is the same object for both names. In that way, Python doesnt have to create a new duplicate object.


## Namespace 
Its a collaction of names. Different namespaces can co-exist at a given time but are completely apart.  

Each module (a file who contain Python code) have his own global namespace, thats why the same name may exist in different modules with out collide.

So, there is 3 level of namespaces in Python:

    Built-in: Is the default namespace and have fuctions like print(), id(), input(), etc
    
    Global: There is one global namespace in each module

    Local: Modules can have various functions or classes into it. So, there will be created a local namespace when the fuction or class is called

## Scope
Even when there are various namespaces defined, we may not be able to access all of them from every part of the program. Its called scope. There is at least, three nested scopes:

    Scope of the current fuction, which has local names  
    Scope of the module which has global names
    Built-in scope which has built-in names

When a reference is made inside a function, the name is searched first in the inside scope and then out. For example, if the reference was made into a function, the first scope to search the name is into the scope of the current function, then, in the global names and at last, in the built-in. 

If there is a function inside another function, a new scope is nested inside the local scope.

## Dynamic typing
Python execute type check only when the code runs, so, it have dinamic typing. It means there can change the type of the var data over its lifetime.

## Type of data
In Python, data can be simple or composed. Simple are bool, string and integer. Composed are list, classes and others.