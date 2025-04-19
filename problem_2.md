<img width="30%" alt="image" src="https://github.com/user-attachments/assets/f3c72433-e460-459c-adfd-00029efd2587">


## Trees

There are two tasks:

### 2.1 Iterative Pre-order and In-order Traversal (30pt) 

Implement the function that returns the values of a pre-order and in-order traversal from a binary tree, respectively.

```c++
template<class T>
std::vector<T> *BinaryTree<T>::dfs_in_order() {
    auto *result = new std::vector<T>();
    /*
     * TODO
     */
    return result;
}
```

and

```c++
template<class T>
std::vector<T> *BinaryTree<T>::dfs_pre_order() {
    auto *result = new std::vector<T>();
    /*
     * TODO
     */
    return result;
}
```

The "dfs" in the function name means both are "Depth First Search" algorithm, with regard to "Breadth First Search".

The recursive solution is trivial. Let's here write the **iterative** solution, which means "no recursion".

From the hint of recursive method, we can infer that a stack would be helpful. The return value is a list that containts the values (not nodes) of the tree nodes in the traversal.

Just to be clear, **no recursion is allowed or zero points will be given**.

### 2.2 Lowest Common Ancestor (20pt) 

Given a binary tree, write code to find the lowest common ancestor (LCA) of two given nodes in the tree.

Incidentally, there is a [leetcode problem of this](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/).

According to the [definition of LCA on Wikipedia](https://en.wikipedia.org/wiki/Lowest_common_ancestor): “The lowest common ancestor is defined between two nodes p and q as the lowest node in T that has both p and q as descendants (where we allow **a node to be a descendant of itself**).”

Tests are provided and also serve as a manual for how the algorithm should work. For example:

```
	      1
             / \
            2   3
           / \   \
          4   5   6

```

In this tree, the LCA of nodes 4 and 6 is 1. The LCA of nodes 4 and 5 is 2. 

This is to be done with recursion. 

***Important Assumptions:***

1. The given two nodes always exist in the given tree.
2. All nodes in a given tree have unique values. 
3. The input tree is NOT necessarily a binary search tree.
