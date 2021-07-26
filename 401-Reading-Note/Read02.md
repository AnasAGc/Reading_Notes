# Test-Driven Development
## structure of a test
A convention widely used is the AAA: Arrange, Act and Assert.

* Arrange: you need to organize the data needed to execute that piece of code (input);

* Act: here you will execute the code being tested (exercise the behaviour);

* Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

One of the things that amaze me about TDD is how we can grow our software design consciously and well, just building what is needed to make the test pass. When we are writing tests we are forced to think about the design first and how we can break it into small pieces.

The greatest advantage about TDD is to craft the software design first
Your code will be more reliable: after a change you can run your tests and be in peace

## Recursion

Recursion is The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function.

In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems. 

The idea is to represent a problem in terms of one or more smaller problems, and add one or more base conditions that stop the recursion.

#### difference between direct and indirect recursion

A function fun is called direct recursive if it calls the same function fun. A function fun is called indirect recursive if it calls another function say fun_new and fun_new calls fun directly or indirectly.