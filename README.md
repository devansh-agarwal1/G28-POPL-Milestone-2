# G28-POPL-Milestone-2

1.) **Problem Statement:** Predicting Password Strength using Pattern Matching

_**Principles of Programming Language Angle:**_
In Principles of Programming Language (POPL), the problem of predicting password strength serves as a practical and relevant application of programming language concepts. The central goal is to use the features introduced in programming languages like Haskell and C++ to create a robust and efficient solution for assessing the strength of passwords. 

_**Prior Solutions**_:
Previously the problem is solved using mathematical and computationally efficient approaches such as probabilistic programming (ML), for example using inference algorithms. These approaches involve  various parameters such as the length of the input password, number of upper-case/lower-case/special-characters/digit characters, etc. 
In our algorithm, we are implementing pattern matching in Haskell and C++ via comparing the input passwords to thousands of most commonly used passwords and categorising them as Strong, Medium and Weak.


2.) **Software Architecture:** Haskell vs C++
We have NOT reused any pre-existing implementation of this problem, neither for C++ nor for Haskell. The pattern-matching approach is a unique approach that we have come up with ourselves. 
The software architecture of our Haskell program is a **simple command-line application** involving the following:-

_**Haskell**_
Higher Order Functions such as 'zip' and 'filter':  They are used in conjunction with list comprehensions, providing a clean and declarative way to express operations on lists.
List Comprehensions: The categorizePassword function uses list comprehensions to create a list of tuples representing common passwords and their similarity scores.
Guard Clauses: Guard clauses are employed in the categorizePassword function to define conditions for different password strength categories.

_**C++**_
Dynamically Allocated List (known as 'vector' in C++)
If-Else statements


3.) _**POPL Aspects**_
Functional Programming Paradigm and Imperative Programming Paradigm: 
a) Haskell is a purely functional programming language, and our code exhibits functional programming principles. Functions are defined and used to calculate the similarity and categorize passwords. Through this paradigm, the code becomes more concise, readable, and secure.
b) C++ is a purely imperative programming language. Similar functions are defined in C++ as well. 

Garbage Collection: 
a) Haskell has automatic garbage collector due to which our code is able to run for huge datasets (upto 1 million strings).
b) The fact that garbage collection in C++ needs to be manually done, makes it difficult for the code to run on huge datasets.

Pattern Matching: Both codes use pattern matching in the calculateSimilarity function by comparing two strings passed as parameters. 
a) Haskell uses in-built functions of zip and filter.
b) C++ uses if else statements and basic logic building.
Pattern matching, being a fundamental property of Haskell, has more advantages being implemented in Haskell than C++.

Lazy Evaluations: 
a) Haskell uses lazy evaluation, and functions like zip and filter work well in a lazy context. They only evaluate elements as needed, leading to more efficient code.
b) C++ doesnt use lazy evaluation, thus making it less efficient in this aspect.

Higher-Order Functions: 
a) The Haskell code utilizes higher-order functions like maximumBy from the Data.List module, which takes a comparison function as an argument.
b) C++ doesn't leverage higher-order functions or functional programming paradigms extensively.

Monadic IO Actions: 
a) In Haskell, The main function is structured using monadic IO actions (do notation) to handle input and output operations.
b) In C++ , we don't have concept of monad as it is not a functional programming language and thus there is no need to emphasize on using pure functions.  

Mutability: 
a) Haskell is immutable by default, meaning that once a value is assigned, it cannot be changed. This improves data security.
b) In C++, by default data is mutable.

Type Inference: 
a) Haskell is statically typed, but our code doesn't explicitly specify types for most variables. This demonstrates Haskell's ability to infer types based on the context.
b) C++ is dynamically typed, which is inconvenient at times.

4.) _**Results**_

HASKELL TEST LOGS:
![Strong_Passwords](https://github.com/devansh-agarwal1/G28-POPL-Milestone-2/assets/119934651/c2d781c3-da5e-4368-ac77-722a7106a1e1)
![Medium_Passwords](https://github.com/devansh-agarwal1/G28-POPL-Milestone-2/assets/119934651/bfcdc522-cb82-461c-a302-5ab950e5c152)
![Weak_Passwords](https://github.com/devansh-agarwal1/G28-POPL-Milestone-2/assets/119934651/37fb989d-4f50-4f6d-9269-af7a22690642)

C++ TEST LOGS:
<img width="817" alt="Medium_Passwords" src="https://github.com/devansh-agarwal1/G28-POPL-Milestone-2/assets/119934651/101190a2-1f5b-4a25-99f4-522da2859f03">
<img width="809" alt="Strong_Passwords" src="https://github.com/devansh-agarwal1/G28-POPL-Milestone-2/assets/119934651/d9500b01-165c-4300-b6b1-28a3826a933e">
<img width="789" alt="Weak_Passwords" src="https://github.com/devansh-agarwal1/G28-POPL-Milestone-2/assets/119934651/6f2b4881-e6e8-44a6-b86b-6e728b3973e1">





5.) _**Potential for future work**_

a) Machine Learning Integration:
Exploring the integration of machine learning models for password strength prediction can significantly enhance the system's accuracy and adaptability. Machine learning algorithms can learn intricate patterns and trends in password data, providing a more nuanced and dynamic approach to strength assessment.

b) Integration with Password Management Tools:
Collaborating with password management tools for seamless integration can have a substantial impact. Users benefit from real-time feedback within their preferred password management applications, promoting secure practices and simplifying the adoption of strong password policies.
