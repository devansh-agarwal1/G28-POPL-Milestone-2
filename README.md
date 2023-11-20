# G28-POPL-Milestone-2

1.) **Problem Statement:** Predicting Password Strength using Pattern Matching

_**Principles of Programming Language Angle:**_
In Principles of Programming Language (POPL), the problem of predicting password strength serves as a practical and relevant application of programming language concepts. The central goal is to use the features introduced in programming languages like Haskell and C++ to create a robust and efficient solution for assessing the strength of passwords. 

_**Prior Solutions**_:
Previously the problem is solved using mathematical and computationally efficient approaches such as probabilistic programming (ML), for example using inference algorithms. These approaches involve  various parameters such as the length of the input password, number of upper-case/lower-case/special-characters/digit characters, etc. 
In our algorithm, we are implementing pattern matching in Haskell and C++ via comparing the input passwords to thousands of most commonly used passwords and categorising them as Strong, Medium and Weak.


2.) **Software Architecture:** Haskell vs C++
We have not reused any pre-existing implementation of this problem. The pattern-matching approach is a unique approach that we have come up with ourselves. 
The software architecture of our Haskell program is a **simple command-line application** involving the following:-

_**Haskell**_
Higher Order Functions such as 'zip' and 'filter':  They are used in conjunction with list comprehensions, providing a clean and declarative way to express operations on lists.
List Comprehensions: The categorizePassword function uses list comprehensions to create a list of tuples representing common passwords and their similarity scores.
Guard Clauses: Guard clauses are employed in the categorizePassword function to define conditions for different password strength categories.

_**C++**_
