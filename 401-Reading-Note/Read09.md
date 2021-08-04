# Classes With Dunder methods

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example \__init__ or \__str__.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are at the end of the day there’s nothing “magical” about them.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:

## Special Methods and the Python Data Model

This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, attribute access, etc.

You can see Python’s data model as a powerful API you can interface with by implementing one or more dunder methods. If you want to write more Pythonic code, knowing how and when to use dunder methods is an important step.

- Object Initialization: \__init__

Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the \__init__ dunder:

```
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
```
The constructor takes care of setting up the object. In this case it receives the owner name, an optional start amount and defines an internal transactions list to keep track of deposits and withdrawals.

- Object Representation: \__str__, \__repr__

It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1. \__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of \__repr__ is to be unambiguous.

2. \__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

implementation:

```
class Account:
    # ... (see above)

    def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)
```

how to call:

```
str(acc)
print(acc)
repr(acc)
```

## Iteration: \__len__, \__getitem__, \__reversed__

In order to iterate over our account object, you need to define the methods above, len is for the array length, get item is to allow to iterate over an arras, and reversed is to reverse an array.

## Operator Overloading for Comparing Accounts: \__eq__, \__lt__

how to implement

```
    def __eq__(self, other):
        return self.balance == other.balance

    def __lt__(self, other):
        return self.balance < other.balance
```

* \__add__ => to add two instances together

* \__call__ => to make the instance callable

# Basic Statistics in Python — Probability

At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur. The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:


Tutorial: Basic Statistics in Python — Probability

When studying statistics for data science, you will inevitably have to learn about probability. It is easy lose yourself in the formulas and theory behind probability, but it has essential uses in both working and daily life. We’ve previously discussed some basic concepts in descriptive statistics; now we’ll explore how statistics relates to probability.


What is probability?

At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur. The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:

* Flipping a heads
* Flipping a tails

These two events form the sample space, the set of all possible events that can happen. To calculate the probability of an event occurring, we count how many times are event of interest can occur (say flipping heads) and dividing it by the sample space. Thus, probability will tell us that an ideal coin will have a 1-in-2 chance of being heads or tails. By looking at the events that can occur, probability gives us a framework for making predictions about how often events will happen. However, even though it seems obvious, if we actually try to toss some coins, we’re likely to get an abnormally high or low counts of heads every once in a while. If we don’t want to make the assumption that the coin is fair, what can we do? We can gather data! We can use statistics to calculate probabilities based on observations from the real world and check how it compares to the ideal.

## Conclusion

We started with descriptive statistics and then connected them to probability. From probability, we developed a way to quantitatively show if two groups come from the same distribution. In this case, we compared two wine recommendations and found that they most likely do not come from the same score distribution. In other words, one wine type is most likely better than the other one. Statistics doesn’t have to be a field relegated to just statisticians. As a data scientist, having an intuitive understanding on common statistical measures represent will give you an edge on developing your own theories and the ability to subsequently test these theories. We barely scratched the surface of inferential statistics here, but the same general ideas here will help guide your intuition in your statistical journey. Our article discussed the advantages of the normal distribution, but statisticians have also developed techniques to adjust for distributions that aren’t normal.