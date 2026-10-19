## Problem Statement:

Design and implement a console-based Grocery List System in C++ using a Singly Linked List. 

The system allows users to add grocery items, display the grocery list, search for items, update quantities, and delete items.

Each node stores the item name, quantity, and a pointer to the next node. 

The linked list allows dynamic memory allocation, making it easy to manage grocery items without a fixed size.

## Approach:

The Grocery List System is implemented in C++ using a Singly Linked List.

Node Creation: Each node stores the grocery item name, quantity, and a pointer to the next node.

Adding Items: A new node is created and added to the end of the linked list.

Displaying Items: The linked list is traversed from the head to the last node to display all grocery items and their quantities.

Searching Items: The program searches for a grocery item by comparing its name with the names stored in the linked list.

Updating Quantity: If the item is found, its quantity is updated with the new value entered by the user.

Deleting Items: The program searches for the required item and removes its node from the linked list.

Menu-Driven System: A menu allows users to select different operations. The program continues until the user selects the Exit option.

Memory Management: Dynamically allocated memory is released after the program exits to avoid memory wastage.

## Complexity:
  
1.Time Complexity

Add Item: O(n) – The program traverses the list to insert an item at the end.

Display List: O(n) – Every node is visited to display the grocery items.

Search Item: O(n) – The program searches each node until the item is found.

Update Quantity: O(n) – The list is traversed to find and update the item.

Delete Item: O(n) – The list is traversed to find and delete the required item.

Here, n represents the total number of grocery items in the linked list.

2. Space Complexity
 
O(n) – Memory is required to store all grocery items in dynamically allocated nodes.

## Conclusion:
   
The Grocery List System was successfully implemented in C++ using a Singly Linked List.

It allows users to add, display, search, update, and delete grocery items.

This project helped in understanding linked list operations, dynamic memory allocation, and memory management in a practical application.
