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
Every value in Python has a datatype. We dont have to forget that everything is an object in Python, so data types are actually classes and vars are instances (objects) of these classes. You can think of a object as a generic container.

    Numbers: int, float, complex
    Strings: Sequence on unicode chatacters
    List: ordered sequence of items. All the items in a list dont need to be the same type
    Tuple: Are ordered sequence of items too but they cant be modifies once created
    Set: Unordered collection of unique items. 
    Dictionary: unordered collection of key-value pairs
    Boolean: Logic value, could be True or False

## Classes 
Are like molds or container who simulate the struct of something. Is a bundle of data of different types and functions logically grouped together.

## Objects 
Are an instances of that molds.  

But, not all objects are created equal!!! Because there is two kinds of objects: Mutable and Inmutable.

* Mutable: list, dict, set, byte aeeay, user-defined classes
* Inmutable: int, float, long, complex, string tuple, bool

But, what does mutable and inmutable means?
Basicaly, the value of the mutable object can be modifies in place after the creation, while the value of the inmutable object can not! 


``` Python 
# "a" is an inmutable object because is an int class type
a = 89
print(id(a)) # 4434330504
a += 1
print(id(a)) # 4430689552  

# "b" is an mutable object because is a list class type
b = [1,2,3]
print(id(b)) # 4430688016
b += [4]
print(id(b)) # 4430688016  
```

  
## Classmethod decorator 
Its a method how belongs to the class and not to the instances. The first argument in the parameter is the reference to a class object. For example:

``` Python 
class Person: 
    def __init__(self, name, age): 
        self.name = name 
        self.age = age 
      
    @classmethod
    def fromBirthYear(cls, name, year): 
        return cls(name, date.today().year - year) 
     
person1 = Person('mayank', 21) 
person2 = Person.fromBirthYear('mayank', 1996) 
  
print (person1.age) # 21 
print (person2.age) # 22
```

## Inheritance
Is when a class uses code who already was constructed in another class. For example:

``` Python 
class Parent: 
    def __init__(self, eye_color, last_name): 
        self.eye_color = eye_color 
        self.last_name = last_name 
    
    def greeting():
        print("Hello")
   
class Child (Parent):
    def __init__(self, eye_color, last_name, hair_color):
        super().__init__(eye_color, last_name) 
        # With super() you can access to the parents methods 
        self.hair_color = hair_color
    
    def something():
        print("Something")

parent = Parent('black','Lopez')
child = Child('black','Lopez', 'black')

parent.greeting() # Hello
child.greeting()  # Hello
child.something() # Somehting


```


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

## Reading errors
Its recommended read the errors from the bottom to the top. This way the message will be easy to understand

## PEP 8 
Is the name of the style guide for Python Code: https://pep8.org/

## Strings
They can be defined by single quote of double quote, but whatever you used, you should be consistent with that. Longs strings can be defined with triple quote (""")

## Is
The operator 'is' is used to make sure if the element have the same memory ref 

## Defaults arguments 
Are arguments declared in the function. They looks like this:
```Python
def foo(name, lastname='Lopez'):
    print('hello', name, lastname)
foo('Mauro') #Will print 'Hello Mauro Lopez'
foo('Felipe','Martinez') #Will print 'Hello Felipe Martinez'
```
If the fuction is called without set the value of the argument, it will be the default declared previusly. 

## Errors and Exceptions
There is at last two distinguishable kind of errors in Python: Syntax error and Execptions. 


 * Syntax error: can't undestand what you are trying to say. For example:  
    ```Python
    print (hello world) 
    ```
 * Execptions: When python understands what you are trying to saying, but get troubles when follow the instructions. For example:
    ```Python
    callMe = "maybe"
    print (callme)
    ```

### Handling Exceptions 
You can hand the exceptions with the help of "try" and "except" keywords.

```Python  
    while (true):
        try: 
            x = int( input ("Please enter a number:" ) )
            break
        except ValueError:
            print("Error! No valid number.")
```
### Raising exceptions
The raise statement allows the programer to force a specified exception to occur.

```Python
response = requests.get('http://example/api')
status_code = response.status_code

if status_code !== 200:
    raise RuntimeError(f"An error ocurred. Status code:"{status_code})
else:
    print (response)    
```

## Comprehensions 
You can avoid the common way of create list by creating it with recursivity. 

From this:
```Python
names = ['Mauro', 'Felipe', 'Bryan', 'Giss', 'Crisly', 'Carlos']
upper_names = []
for name in names:
    upper_case_name = name.upper()
    upper_names.append(upper_case_name)
print(upper_names)
```

To this:
```Python
upper_names = [name.upper() for name in names]
print (upper_names)
```

You can add conditionals too:

```Python
upper_names = [name.upper() for name in names if name != "Mauro"]
print (upper_names)
```
## Zip
Its an object how contains tuples created by the union of lists. 

```Python
name = ("Mauro", "Marco", "Bryan")
second_name = ("Alberto", "Felipe", "", "Vicky")
last_name = ("Lopez", "Martinez","Arrieta")
complete_name = zip(name, second_name, last_name)
print(list(complete_name)) # [('Mauro', 'Alberto', 'Lopez'), ('Marco', 'Felipe', 'Martinez'), ('Bryan', '', 'Arrieta')]
```

## Dir
type 'dir' and into parenthesis an object (or a data type like str, int, list, etc) it will show a list of valid attributes for that object. 
```Python
print(dir(list))
```

## Help


## Dynamic typing
Python execute type check only when the code runs, so, it have dinamic typing. It means there can change the type of the var data over its lifetime.

## Type of data
In Python, data can be simple or composed. Simple are bool, string and integer. Composed are list, classes and others.

### Just to know 
* 0 (the int value) can be taken as False and any other number can be taken as True

* In cycles, you can interact with the flow of the iteration with "continue" and "break". Continue will jump into the beginning of the cycle just after the interpreter read the stament and break will end with the cycle.



## Resources

### Learning python with Ninna from Frontend Master 
    https://www.learnpython.dev/

