# Ch02 Complexity

## What is complexity theory?

You think about complexity in terms of **time** as you **scale** the **inputs** that go into the algorithm you are using to solve the problem.

## What is P-Time?

When the complexity of an algorithm scales according to a **polynomial equation**

### What is a polynomial?

Expression consisting of variables and coefficients. It only employs the operations of additional, subtraction, multiplication, and non-negative integer exponents.

**What is an example of a polynomial of a single value?**

```
x2 - 4x + 7
```

**What is an example of a polynomial of multiple variables**

```
x3 + 2xyz2 - yz + 1
```

### What is the P Complexity Class?

Describes the set of all problems solvable in P time

## What is Exp time?

Exponentially complex

### What is an example of an equation on Exp time?

```
T = 2^n
```

## What is R time?

R represents all of the problems that are solvable in finite time

## List and define the 3 main complexity classes

* P: set of problems solvable in polynomial time - easy
* Exp: set of problems solvable in exponential time - hard
* R: all solvable problems

## What is Determinism?
When you execute a routine and get a result and then, based on that result, execute another routine, then another, etc. Each result links together until we find an answer.

## What is Nondeterminism?

When you execute a routine and get a result, then execute one of a series of next steps. You don't know which next step from the series will be executed, it will be decided at the time. This repeats until you arrive at an answer. When you have an answer, there is no way of determining how you got there.

It uses a series of lucky guesses or random change (each of which is always correct) to figure out the answer to a given program. You can solve an exponentially complex problem in P time.

## What does it mean to say a problem is an NP problem?

That problem is solvable in P time given a nondeterministic algorithm.

## When is a problem NP?

A problem is NP if it is:
* Solvable in exponential time (Exp)
* Verifiable in polynomial time (P)
* Also solvable in polynomial time by nondeterministic methods

### What does it mean to say that a problem is NP-Hard?

A NP-Hard problem can be reduced to other problems in NP, but are not within NP themselves.

### What does it mean to say that a problem is NP-complete?

An NP-Complete problem is a decision problem classifiable in NP.

**What kind of problem is almost always NP-complete? Why?**

Decision problems - you are able to verify the answer to the problem

## What kind of problem is a combinatorial problem?

NP-Hard

## What is the Cook-Levin Theorem?

Any problem in NP can be reduced to the boolean satisfiability problem.

## What is the Boolean Satifiability Problem?

Asks whether the variables of a given boolean formula can be consistently replaced by values TRUE and FALSE in such a way that formula evaluates to TRUE.