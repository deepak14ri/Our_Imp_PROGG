Classes and Objects I
TUTORIAL
Python Classes and Methods
Python is an “object-oriented programming language.” This means that almost all the code is implemented using a special construct called classes. Programmers use classes to keep related things together. This is done using the keyword “class,” which is a grouping of object-oriented constructs.

By the end of this tutorial you will be able to:

Define what is a class
Describe how to create a class
Define what is a method
Describe how to do object instantiation
Describe how to create instance attributes in Python
What is a class?
A class is a code template for creating objects. Objects have member variables and have behaviour associated with them. In python a class is created by the keyword class.

An object is created using the constructor of the class. This object will then be called the instance of the class. In Python we create instances in the following manner

Instance = class(arguments)
How to create a class
The simplest class can be created using the class keyword. For example, let's create a simple, empty class with no functionalities.

>>> class Snake:
...     pass
... 
>>> snake = Snake()
>>> print(snake)
<__main__.Snake object at 0x7f315c573550>
Attributes and Methods in class:
A class by itself is of no use unless there is some functionality associated with it. Functionalities are defined by setting attributes, which act as containers for data and functions related to those attributes. Those functions are called methods.

Attributes:
You can define the following class with the name Snake. This class will have an attribute name.

>>> class Snake:
...     name = "python" # set an attribute `name` of the class
...
You can assign the class to a variable. This is called object instantiation. You will then be able to access the attributes that are present inside the class using the dot . operator. For example, in the Snake example, you can access the attribute name of the class Snake.

>>> # instantiate the class Snake and assign it to variable snake
>>> snake = Snake()

>>> # access the class attribute name inside the class Snake.
>>> print(snake.name)
python
Methods
Once there are attributes that “belong” to the class, you can define functions that will access the class attribute. These functions are called methods. When you define methods, you will need to always provide the first argument to the method with a self keyword.

For example, you can define a class Snake, which has one attribute name and one method change_name. The method change name will take in an argument new_name along with the keyword self.

>>> class Snake:
...     name = "python"
...     
...     def change_name(self, new_name): # note that the first argument is self
...         self.name = new_name # access the class attribute with the self keyword
...
Now, you can instantiate this class Snake with a variable snake and then change the name with the method change_name.

>>> # instantiate the class
>>> snake = Snake()

>>> # print the current object name 
>>> print(snake.name)
python

>>> # change the name using the change_name method
>>> snake.change_name("anaconda")
>>> print(snake.name)
anaconda
Instance attributes in python and the init method
You can also provide the values for the attributes at runtime. This is done by defining the attributes inside the init method. The following example illustrates this.

class Snake:

    def __init__(self, name):
        self.name = name

    def change_name(self, new_name):
        self.name = new_name
Now you can directly define separate attribute values for separate objects. For example,

>>> # two variables are instantiated
>>> python = Snake("python")
>>> anaconda = Snake("anaconda")

>>> # print the names of the two variables
>>> print(python.name)
python
>>> print(anaconda.name)
anaconda
