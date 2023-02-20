# How to code review

This document contains a couple of suggestions for systematically reviewing code.

## Test

Download the code to your machine and install the project requirements if there are any.

* Does it run?
* Is the compiler/interpreter throwing error messages?
* If there are errors: Do you understand what they are saying and why they are happening? (If not: The internet is good starting point for trying to figure out what is going on.)
* Does the code do what it claims to do?
* If it's doing something unexpected: Note this for the next step.

## Read through the code: Semantics

* Do you understand what it does? Try to go through it systematically:
  * Do you understand what each function is doing?
  * Are there potential endless loops?
  * Are there potential unhandled errors that may be caused by unexpected input? (Python is fairly robust in this regard. Meaning, as a dynamically typed language, it would interpret variables in way that don't break the program whenever possible. That the programm is running doesn't necessarily mean that it is doing the correct thing though.)
* If you noticed anything weird while testing: Can you see where it is coming from?

## Read through the code: Style

Bad style makes code difficult to read and understand, which results in difficult to maintain and error-prone code.
While reading keep an eye for following:
* Do variables, functions, and classes have readable, non-misleading, and unambiguous names?
* Is there proper spacing which makes the code more readable?
* If there are comments: Are those correct and up-to-date? Do they explain why something is being done vs how? (The code itself shows you how.)
* Are there things done in a unnecessary complex way?
* Do you notice repeating fragments that can be abstracted in a function and re-used?

## Check further meta information

* If the code has been committed to a version control system and there are multiple commits: Check the commit messages. Ideally, the author has described in them what they've changed and why.

