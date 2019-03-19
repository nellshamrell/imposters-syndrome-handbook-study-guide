# Ch03 Lambda Calculus

## What is lambda calculus?

A simple notation for functions and application that describes formal mathematical logic.

## What is a lambda?

An anonymous function that can be thought of as a value

## What are the rules of lambda calculus?

* Only functions, nothing else. No data types of any kind (no numbers or types).
* Can substitute functions using variables (function can be treated as a value).
* Can combine multiple terms in lamda calculus to create a high order function called a combinator.

## Label the parts of this function

&#955;x.x

&#955; is the function notation

The first x is the argument

The second x is the body/return

## What is this expression referred to as? Why?

&#955;x.x

I combinator.  The identity function - whatever you pass it is returned.

## What does this function do?

&#955;x.x (y)

Applies the value y to the function. It will substitute all occurences of x with y.

## What does this function do?

&#955;x.y (z)

It will return y.

## What is this expression referred to as? Why?

&#955;x.y (z)

Constant function

It always returns the constant value of y - doesn't matter what you pass it.

## In this equation, what is the bound variable? Why is a bound variable?

&#955;x.y

x is the bound variable - it is the function head of the argument and bound to the expression. I can substitute x in this function if and only if I make sure to substitute every occurence of the bound variable x.

## In this equation, what is the free variable? Why is it a free variable?

&#955;x.y

y is the free variable - it is not bound to any lambda function.

## What is substitution in lambda calculus?

When you apply a value to a function, you substitute that value in the funbction itself. Substitution is **left-applicative** - you start on the left and move to the right as required.

## What will happen in this function?

&#955;x.x 3

All **bound** occurences of x will be replaced with 3 in the body, x.

## What does it mean to say that functions in lamdba calculus only have an arity of 1?

It can only have one argument or one bound variable.

## What is currying?

Breaking a function with multiple arguments into chained functions with an arity of 1.

## How would you curry this function? How would you describe it in words?

&#955;xy.t

&#955;x.&#955;y.t

&#955;x now has a body of &#955;y.t

## How would you reduce this function?

&#955;x.(&#955;y.y x)

Replace all instances of y in &#955;y.y with x.

&#955;y.y will then return x

So this can be reduced to:

&#955;x.x

## What is Church Encoding?

Representations for values and operations. It allows us to use booleans, numbers, conditional statements, and loops to construct **combinators**.

## What are combinators?

Combinations of smaller functions that do a thing. They are higher order functions that use only function application and earlier defined combinators to define a result from its arguments. They use lambda expressions and bound variables, nothing else.

### What is the Omega combinator? Give an example.

It is the "looping" combinator - it allows for recursively looping over a given function. The function will not only return what it is given, it will also return its replicator.


&#955;x.xx  &#955;x.xx

### What is the Y combinator? Give an example.

It is a recursive, fixed point function. You give it a function as an argument, which it invokes, then it returns the function back to you.

Y = &#955;xf.(&#956;x.f(xx))(&#955;x.f(xx))

### How is the Y Combinator different from the Omega Combinator?

Instead of just replicating xx, y0uo are replication the application f(xx) where f is the initial function itself. It allows you to parse a second expression, which represents the number of times you want the loop to execute. You use it with functions you iterate over.