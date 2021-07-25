![img](https://www.xenonstack.com/images/insights/2020/12/xenonstack-functional-programming.png)
## What is functional programming?
Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 

## What is a pure function and how do we know if something is a pure function?
pure functions will return the same result if given the same arguments , in other words it doesn't depend on global variables , If our function reads external files, it’s not a pure function — the file’s contents can change.

Example:
	
	    const summation = (a,b) => a+b ;	


## What are the benefits of a pure function?
The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:

        Given a parameter A → expect the function to return value B
        Given a parameter C → expect the function to return value D

## What is immutability?
Unchanging over time or unable to be changed.When data is immutable, 
its state cannot change after it’s created. If you want to change an immutable object,
 you can’t. Instead, you create a new object with the new value.

## What is Referential transparency?
if a function consistently yields the same result for the same input,
 it is referentially transparent.
 