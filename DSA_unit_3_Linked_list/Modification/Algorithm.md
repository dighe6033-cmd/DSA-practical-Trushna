## Algorithm:

Step 1: Start the program.

Step 2: Define a node containing the item name, quantity, a pointer to the next node, and a pointer to the previous node.

Step 3: Initialize the head pointer to NULL.

Step 4: Display the menu with the following options:

Add Item

Display List

Search Item

Update Quantity

Delete Item

Exit

Step 5: Accept the user's choice.

Step 6: Perform the selected operation.

Add Item: Accept the item name and quantity, create a new node, and insert it at the end of the doubly linked list. Update both next and prev pointers.

Display List: Traverse the list using the next pointer and display all items with their quantities.

Search Item: Search for the specified item and display its quantity if found.

Update Quantity: Search for the item and update its quantity.

Delete Item: Find the item, adjust the next and prev pointers of neighbouring nodes, and delete the selected node.

Exit: Display the exit message and terminate the menu loop.

Step 7: If the choice is invalid, display an appropriate error message.

Step 8: Repeat Steps 4–7 until the user selects Exit.

Step 9: Delete all remaining nodes and release the allocated memory.

Step 10: Stop the program.
