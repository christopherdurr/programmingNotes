#Big O Notation
Notes done by: 
* Christopher Durr

Also known as Landau's symbol

f(x) = O(g(x))

**Notation**|**Name**

* O(1)		   Constant

* O(logn)		Logarithmic

* O(log n<sup>c</sup>)	Polylogorithmic

* O(n)		   Linear

* O(n<sup>2</sup>)		   Quadratic

* O(n<sup>c</sup>)		   Polynomial

* O(c<sup>n</sup>)		   Exponential


Note that O(c<sup>n</sup>)) grows faster than O (n<sup>c</sup>))

* A function that grows faster than a power of n is **superpolynomial**
* A function slower than c<sup>n</sup> is **subexponential**
* e.g. Integer Factorization is both superpolynomial and subexponential

When given multiple terms, use the term that grows the fastest

e.g. f(n) = 10logn + 5logn + 7n + 3n^2 + 6n^3

Other Notation:

**Theta** 

f(n) = theta(g(n))
* f(n) = O(g(n))
* g(n) = O(f(n))

Using theta notation to describe complexity is a stronger claim than O notation

Performance v. Complexity

Complexity of an algorithm affects performance but not the other way around. 
Performance is dependent on external factors like speed of CPU. 

If a function always performs the same operation, it is said to take **constant time**

We are interested in the worst-case scenario. That is, T(n) <= c * F(n)

Example:

T(n) = 3n^2 + 5

T(n) is O(n^2) because 3n^2 + 5 < 4n^2

Therefore 4n^2 is worst case. 



Determining Complexities 
* Sequence of Statements
    *    Total time is found by time for all statements
    *     If each statement is "simple" then total time is O(1)
* if/else statements
    *     Either block 1 or block 2 will execute
    *     Worst case time is the slower of two possibilities
    *     e.g. if block 1 takes O(1) time and block 2 takes O(n) time, then it is O(n)
* Loops
    *     Loop executes n times
    *     If statements within loop are O(1) then total time is O(n)
* Nested Loops
    *     If both loops execute n times, O(n^2)
    *     else, O(n*m) where 1st loop executes n times and 2nd loop executes m times



