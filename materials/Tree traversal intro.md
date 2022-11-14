This is a very brief explanation of the main ideas of **tree traversals**. 

## What is a tree traversal?

You know what a *tree* is (it's a connected graph that has no cycles). You also know that they are used practically everywhere in computer science as a way of organizing and storing data. Most recently we looked at [binary search trees](https://www.geeksforgeeks.org/binary-search-tree-data-structure/) in class and used BSTs to take totally ordered data and store it in a particular way. 

The flip side of storing that data, is accessing it and turning it into a list. The way we do this is to **visit the nodes of the tree one at a time in a particular order**. This process of visiting the nodes (and adding them to an output list as we visit) is called a **tree traversal**. 

## What problem does a tree traversal solve? 

For example, suppose you have this BST of words that are ordered [lexicographically](https://stackoverflow.com/a/60604165): 



Let's suppose we want to produce a list of all 15 words in this BST in alphabetical/lexicographic order. We don't know the order in which the words were entered into the tree. But we can traverse the tree according to a particular method or algorithm: For each subtree, do the following recursively: 

- Visit the left subtree
- Then visit the parent node of the subtree
- Then visit the right subtree

This method of traversal is called an _in-order traversal_. 

On the other hand, look at this BST which encodes the steps in a `while` loop, so that a computer or calculator can execute it: 


(Credit: https://agilewarrior.wordpress.com/2017/11/07/binary-trees/)

For a computer to make sense of, or **parse**, this expression, it must go through the nodes of the tree one by one in a particular order and make simple computations where it can. So first it would need to visit the left subtree, visit the leaves (loading `x` and `0` into memory) and then visit the parent node to compare the two. Then it visits the parent node of that left subtree to run the `while` statement. Then it recursively visits all the nodes of the right subtree, one by one (leaf -> parent -> leaf) and executes single statements one at a time. This too is a traversal -- visiting the nodes of the tree one at a time to produce a list of operations that the computer can comprehend. 

## Learning the traversal methods

In the videos for today's lesson, you'll learn three methods of traversing a tree: 

- *Pre-order* traversal
- *In-order* traversal
- *Post-order* traversal

Each method works slightly differently to produce different results that are of use in different situations. 
