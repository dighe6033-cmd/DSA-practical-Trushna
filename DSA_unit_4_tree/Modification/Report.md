## Problem Statement:

Write a C++ program to construct a Binary Search Tree (BST) for student record management.

Store each student's name along with their roll number and implement insertion, searching, updating, and deletion of student records.

Display all student records in ascending order of roll numbers.

## Approach:

The Student Record Management System is implemented using a Binary Search Tree (BST) in C++.

Node Creation: Each node stores the student's roll number, name, and pointers to the left and right child nodes.

Insertion: A new student record is inserted according to the roll number.

Smaller roll numbers are placed in the left subtree, while larger roll numbers are placed in the right subtree.

Searching: The program searches for a student record using the roll number and displays the details if the record is found.

Updating: The program searches for the given roll number and updates the student's name if the record exists.

Deletion: The program deletes a student record using its roll number. It handles nodes with no children, one child, or two children.

Displaying Records: Inorder traversal is used to display all student records in ascending order of roll numbers.

Menu-Driven Operations: A menu allows the user to perform different operations repeatedly until the Exit option is selected.

## Complexity:

The time complexity of the Student Record Management System depends on the height of the Binary Search Tree (BST).

1.Insertion:
   
Average Case: O(log n)
   
Worst Case: O(n)

2.Searching:

Average Case: O(log n)

Worst Case: O(n)

3.Updating:

Average Case: O(log n)

Worst Case: O(n)

4.Deletion:

Average Case: O(log n

Worst Case: O(n)

5.Displaying Records:

Time Complexity: O(n), because every student record is visited during inorder traversal.

6.Space Complexity:

O(n), because memory is required to store all student records in the BST.

## Conclusion:

The Student Record Management System was successfully implemented using a Binary Search Tree in C++.

The program allows users to insert, search, update, delete, and display student records in ascending order of roll numbers.

This project helped in understanding BST operations, tree traversal, recursion, and dynamic memory allocation.
