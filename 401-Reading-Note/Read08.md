# List Comprehensions in Python

List comprehensions provide a concise way to create lists.

It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists.

The result will be a new list resulting from evaluating the expression in the
context of the for and if clauses which follow it.

The list comprehension always returns a result list.

## Syntax

The list comprehension starts with a ‘[‘ and ‘]’, square brackets, to help you remember that the
result is going to be a list.

```
[ expression for item in list if conditional ]
```
is equal to
```
for item in list:
    if conditional:
        expression
```

## Examples

* create squares

```
squares = [x**2 for x in range(10)]
print squares
# this will give this result
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

* Show the first letter of each word

```
listOfWords = ["this","is","a","list","of","words"]

items = [ word[0] for word in listOfWords ]

print items
```
the output is ``` [‘t’, ‘i’, ‘a’, ‘l’, ‘o’, ‘w’] ```

* Print numbers only from a given string

```
    string = "Hello 12345 World"
    numbers = [x for x in string if x.isdigit()]
    print numbers
```

* Using list comprehension in functions

```
def double(x):
  return x*2
print double(10)
```
you can use comprehension to apply double function on a wide range of values

```
[double(x) for x in range(10)]
```