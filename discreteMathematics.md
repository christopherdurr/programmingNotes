# Chapter 2

## Chapter 2.1: Sets

A **set** is an unordained collection of objects, called *elements* or *members* of the set. 

a ∈ A denotes that a is an element of set A

Ex. The set V of all vowels is V = {a,e,i,o,u}

Sets can have completely unrelated elements. For instance, {2, John, pi, z} is a set

**Set Builder Notation**

Ex. O =  {x | x is an odd positive integer less than 10}

There are several sets that play a key role in discrete mathematics:

* N: Set of natural numbers
* Z: Set of integers
* Z+: Set of positive integers
* Q: Set of rational numbers
* R: Set of real numbers
* R+: Set of positive real numbers
* C: Set of complex numbers

Two sets are equal if they have the same elements

**Empty Set**/**Null Set**: A set that has no elements

**Singleton Set**: A set with a single element

**Subset**: A ⊆ B. Every element of A is also in B

For every nonempty set S, it is guaranteed to have at least two subsets: 
* The empty set
* The set itself

Put simply, ∅ ⊆ S and S ⊆ S

**Proper Subset**: A ⊂ B and A /= B

**Cardinality**: Number of elements of the set

**Power Set**: Given a set S, the power set is the set of all subsets of the set S. It is denoted by P(S).

A set with n elements has 2<sup>n</sup> elements in the power set.

**Truth Set**: A mathematical or logical set containing all the elements that make a given statement of relationships true when substituted in it. 

## Chapter 2.2: Set Operations

**Union of sets**: A ∪ B. Set that contains the elements in either A or B, or in both

Union of {1, 3, 5} and {1, 2, 3} is {1, 2, 3, 5}

**Intersection of Sets**: A ∩ B. Set containing elements in both A and B. 

Two sets are *disjoint* if their intersection  is the empty set. 

|A ∪ B|=|A|+|B|−|A ∩ B|

A - B: The set containing those elements that are in A but not in B. 

The complement of the set A is U - A

## Chapter 2.3: Functions

Let A and B be nonempty sets. A function F from A to B is an assignment of exactly one element of B to each element of A. F(a) = F(b) if b is the unique element of B assigned by the function F for the elment a of A

This is also known as **mappings** or **transformations**

If F is a function from A to B then A is the *domain* of F and B is the *codomain* of F. 

The *range*, or *image*, of F is the set of all images of the elements of A

If F(a) = B then B is the *image* of A and A is the *preimage* of B. 

If there are F<sub>1</sub> and F<sub>2</sub> as functions. F<sub>1</sub> + F<sub>2</sub> and F<sub>1</sub>F<sub>2</sub> are all functions. 

**One to One**/**Injunction**: A function implies a = b for all a and b in the domain of F. 



