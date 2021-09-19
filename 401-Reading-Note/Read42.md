# Dunder Methods

### Dunder Methods (magic methods)
special methods are a set of predefined methods .they start and end with double underscores, for example __init__ or __str__.

### Dunder Methods :
Object Initialization( \__init__) :
- The \__init__ is a constructor takes care of setting up the object , resave the variable and save the in the object , the input of this method can have a default value this way :
`def __init__(self, amount=0):`
Object Representation( \__str__, \__repr__) :
- \__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of \__repr__ is to be unambiguous.
- \__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.


### **Iteration: (\__len__, \__getitem__, \__reversed__)**
- Len : present the number of items in the object
- Getitem : used to git item at specific index using square brackets
Reversed : used to iterate over transactions in reversed order 

### **perator Overloading for Comparing Accounts: (\__eq__, \__lt__)**
- \__eq__ : used to check the equality of two different objects of the same class, and works when == used
- \__lt__ :used to compare between two different objects of the same class, and works when > or < used

**Operator Overloading for Merging Accounts: \__add__ :**
It used when we adding two objects of the same class  with the + (plus) operator

Callable Python Objects: \__call__:
You can make an object callable like a regular function by adding the \__call__ dunder method.


Context Manager Support and the With Statement: \__enter__, \__exit__
A context manager is a simple “protocol” (or interface) that your object needs to follow so it can be used with the with statement.

**Python Iterators**
Objects that support the \__iter__ and \__next__ dunder methods automatically work with for-in loops.
