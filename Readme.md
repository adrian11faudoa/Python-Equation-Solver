Subject:

An interface is like a blueprint for a class. 
An interface contains a set of methods and properties that a class should implement.

Unlike other programming languages, Python does not implement interfaces in its core language, but the Python standard library allows you to define interfaces in a simple way.

ABC stands for Abstract Base Classes. 
The ABC class enables you to turn a regular class into an abstract class, which is a class that acts as a blueprint for concrete classes.


You can import a specific object x from a module y following the import construct "from y import x"
Example Code:
```
    from abc import ABC
```


In order to be recognized as an abstract method, a method should be decorated with the @abstractmethod decorator.

A decorator is used in Python to modify the behavior of a function. Here's an example of how to use a decorator named spam:
Example Code:
```
    @spam
    def foo():
        pass
```


In Python, data types are recognized during runtime (when the code is executed). 
Therefore, you don't have to specify the data type of a variable when you declare it. 
Nonetheless, you can annotate a variable to clarify that it will hold a specific data type with 
variable: <data type> = value 
or just 
variable: <data type>. 
Note that the Python interpreter does not enforce the types used to annotate variables, and normally you'd need external tools to do it.


The __init_subclass__ method is called whenever the class that defines it is subclassed and it enables to customize the child classes. 
The method takes a parameter named by convention cls (standing for "class"), which represents the new child class.


The hasattr built-in function takes an object as its first argument and a string representing an attribute name as its second argument. 
It returns a boolean indicating if the object has the specified attribute.


the * operator  make it accept a variable number of arguments
Example Code:
```
    def __init__(self, *args):
        pass
```     

The isinstance() built-in function takes two arguments and returns a Boolean indicating if the object passed as the first argument is an instance of the class passed as the second argument.
Example Code:
```
    isinstance(7, int) # True
```

self.coefficients = {self.__class__.degree - i: coef for i, coef in enumerate(args)}
                

The number sign is displayed by default only if negative.
To change this behavior, you can write a colon after the expression to be evaluated within the curly braces of your f-string, and specify the option +. 
This will allow you to display the sign both for positive and negative numbers.
Example Code:
```
    terms.append(f'{coefficient:+}')
```


The sub function from the re module enables you to replace text inside a string based on a regex pattern.
Example Code:
```
    verse = 'Always look on the bright side of life'
    spam = re.sub('bright', 'spam', verse)
    spam == 'Always look on the spam side of life' # True
```
It takes three arguments: the regex pattern to match, the replacement, and the string on which you want to perform the replacement.

Step 35






















