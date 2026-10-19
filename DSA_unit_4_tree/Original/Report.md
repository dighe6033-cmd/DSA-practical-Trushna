## Problem Statement:

Write a C++ program to construct a Binary Search Tree (BST) using student roll numbers and implement insertion, searching, and inorder display operations.

## Approach:

A Binary Search Tree (BST) is used to store student roll numbers.

Each node contains a roll number and pointers to its left and right child nodes.

The insertion operation places smaller roll numbers on the left and larger roll numbers on the right.

The searching operation compares the required roll number with the current node and searches the appropriate subtree.

Inorder traversal (Left → Root → Right) displays roll numbers in ascending order.

A menu-driven program allows the user to insert, search, display, and exit.

## Complexity Analysis:

Time Complexity:

Insertion: O(log n) on average and O(n) in the worst case.

Searching: O(log n) on average and O(n) in the worst case.

Inorder Traversal: O(n), as every node is visited once.

Space Complexity:

BST Storage: O(n), as memory is required for all nodes.

Recursive Operations: O(log n) on average and O(n) in the worst case due to the recursion stack.

Here, n represents the number of student roll numbers stored in the BST.

## Conclusion:

The Student Roll Number Management System was successfully implemented using a Binary Search Tree in C++. 

It allows users to insert, search, and display roll numbers in ascending order. 

This program helped in understanding BST operations, tree traversal, and the use of trees in data management.
