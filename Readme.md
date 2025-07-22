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


In a regex pattern, a lookaround is an assertion that matches a certain pattern without consuming characters in the string. 
One kind of lookaround is the lookbehind, which can be either positive or negative. 
They are denoted by (?<=...) and (?<!...), respectively.
Example Code:
```
    spam = 'black back bat'
    re.sub('(?<=l)a', 'o', spam) == 'block back bat' # True
    re.sub('(?<!l)a', 'o', spam) == 'black bock bot' # True
```
In the example above, the pattern (?<=l)a contains a positive lookbehind, which is used to match the a character only when preceded by an l. 
In the last line of the example, the pattern (?<!l)a contains a negative lookbehind, which is used to match the a character only if it is not preceded by an l. 
Note how, in both cases, the character contained in the lookbehind is not consumed.
Example Code:
```
    re.sub(r'(?<!\d)1', '', equation_string.strip('+'))
```


Another kind of lookaround assertion is the lookahead.
Positive and negative lookahead are denoted by (?=...) and (?!...), respectively. 
They are used to match a pattern if followed by a certain sequence of characters, which is not consumed:
Example Code:
```
    spam = 'black back bat'
    re.sub('a(?=t)', 'o', spam) == 'black back bot' # True
    re.sub('a(?!t)', 'o', spam) == 'block bock bat' # True
```
In the example above, the pattern a(?=t) contains a positive lookahead, which is used to match the a character only when followed by a t. 
In the last line of the example, the pattern a(?!t) contains a negative lookahead, which is used to match the a character only if not followed by a t. 
Again, in both cases, the character contained in the lookahead is not consumed.
Example Code:
```
    re.sub(r'(?<!\d)1(?=x)', '', equation_string.strip('+'))
```


An interesting feature of f-strings is the capability of forcing the output to be right/left-aligned, or centered.
After the expression to be evaluated is inside the curly braces, you need to write a colon followed by an alignment option (< to left-align, > to right-align, ^ to center) and a number representing the width, that is the number of characters in which you want to arrange the text.
Example Code:
```
    f'{"Hello World":>20}'
```
Printing the string from the example above would result in right-aligned text arranged in a space of 20 characters.


Between the colon and the alignment option, you can specify a fill character, which will be used to fill the space around the text within the specified width.


Another feature of f-strings enables you to convert the content of the replacement field (the curly braces) into a string by using a ! followed by the conversion type s. 
For example, f'{obj!s}' converts obj into a string and it is equivalent to f'{str(obj)}'.


Structural pattern matching is a Python construct that enables matching a pattern with a subject value, which is specified after the match keyword:
Example Code:
```
    match value:
        case x:
            <code>
        case y:
            <code>
```
Each pattern is specified after the case statement. 
If the match is positive, the code inside the case block is run.


f-strings also enable you to set a specific precision to your numerical data by using the .nf format specifier, where n is the number of decimal digits to display.
Example Code:
```
    points = f"x: {x}, y: {y:.2f}"
```


The structural pattern matching enables you to verify that the subject has a specific structure. 
In addition to that, it binds names in the pattern to elements of the subject.
Example Code:
```
    match my_list:
        case [a]:
            print(a)
        case [a, b]:
            print(a, b)
```

