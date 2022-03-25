# Trees

## what is Tree in Data Structure? 

*A Tree is a nonlinear hierarchical data structure that consists of nodes connected by edges.*
![Tree](https://cdn.programiz.com/sites/tutorial2program/files/tree_0.png)

## Why Tree Data Structure?

Arrays, linked lists, stacks, and queues are examples of linear data structures that store data sequentially. The temporal complexity of performing any operation in a linear data structure increases as the data amount grows. However, in today's computing environment, this is unacceptable.Because it is a non-linear data structure, different tree data structures provide for faster and easier access to the data.

## Tree Common Terminology:

+ **Node :** A Tree node is a component which may contain its own values, and references to other nodes.
+ **Root :** The root is the node at the beginning of the tree. 
+ **K :** A number that specifies the maximum number of children any node may have in a `k-array` tree.
+ **Left :** A reference to one child node, in a binary tree.
+ **Right :** A reference to the other child node, in a binary tree.
+ **Edge :** The edge in a tree is the link between a parent and child node.
+ **Leaf :** A leaf is a node that does not have any children.
+ **Height :** The height of a tree is the number of edges from the root to the furthest leaf.

![Sample Tree](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

## Traversals:

The ability to traverse trees is a fundamental component of them. We may search for a node, print the contents of a tree, and much more by traversing a tree! When it comes to trees, there are two types of traversals:
+ **Depth-First Search (DFS)**
+ **Breadth-First Search (BFS)**

## Depth-First Search (DFS)

When using depth first traversal, we emphasize traveling through the tree's depth (height) first. There are several methods for performing depth first traversal, each of which alters the order in which we search for/print the root. 

![Depth-First Search (DFS)](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)
**Here are three strategies for traversing depth first:**
+ **Pre-order:** `root >> left >> right` ,Eample: `A, B, D, E, C, F` 
+ **In-order:** `left >> root >> right` ,Eample: `D, B, E, A, F, C`
+ **Post-order:** `left >> right >> root` ,Eample: `D, E, B, F, C, A`

Recursion is the most popular method of traversing a tree. When we reach the end of a sub-path in these traversals, we rely on the call stack to traverse back up the tree.

## Breadth-First Search (BFS)

The algorithm for traversing or exploring tree or graph data structures is called breadth-first search (BFS). It starts at the tree root (or an arbitrary node in a graph, referred to as a'search key') and investigates the neighbors first, before continuing on to the next level neighbors.

![Algorithm Visualization](https://upload.wikimedia.org/wikipedia/commons/5/5d/Breadth-First-Search-Algorithm.gif)

Traditionally, breadth first traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree.