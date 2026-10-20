## Problem Statement:

Design and implement a menu-driven Grocery List System using a doubly linked list in C++. 

The system should allow users to add, display, search, update, and delete grocery items while managing memory efficiently

## Approach:

The Grocery List System is implemented using a Doubly Linked List in C++. Each node stores the grocery item name, quantity, and two pointers: next and prev.

The program uses separate functions to perform the following operations:

1.Add Item: Creates a new node and inserts it at the end of the list.

2.Display List: Traverses the list using the next pointer and displays all grocery items.

3.Search Item: Searches for an item by its name and displays its quantity.

4.Update Quantity: Searches for an item and updates its quantity.

5.Delete Item: Removes the selected item and adjusts the next and prev pointers.

6.Memory Management: Frees the allocated memory when the program exits.

A menu-driven interface allows users to select and perform the required operations.

## Complexity:
   
Let n represent the number of grocery items in the list.

1.Insertion at the End: O(n)

2.Display List: O(n)

3.Search Item: O(n)

4.Update Quantity: O(n)

5.Delete Item: O(n)

6.Space Complexity: O(n)

The time complexity of insertion at the end is O(n) because the program traverses the list to find the last node.

Searching, updating, and deleting also require traversal to locate the item.

The space complexity is O(n) because each grocery item requires one node in memory.

## Conclusion:

The Grocery List System was successfully implemented using a doubly linked list in C++. 

It supports adding, displaying, searching, updating, and deleting grocery items.

This project demonstrates linked list operations, pointer handling, dynamic memory allocation, and efficient memory management.
