#include <iostream>
#include <string>
#include <limits>
using namespace std;

struct Node {
    string name;
    int quantity;
    Node* next;
    Node* prev;
};

Node* head = NULL;

// Add grocery item
void addItem() {
    Node* newNode = new Node;

    cout << "Enter item name: ";
    cin >> ws;
    getline(cin, newNode->name);

    if (newNode->name.empty()) {
        cout << "Item name cannot be empty.\n";
        delete newNode;
        return;
    }

    cout << "Enter quantity: ";

    if (!(cin >> newNode->quantity) ||
        newNode->quantity <= 0) {
        cout << "Invalid quantity!\n";
        cin.clear();
        cin.ignore(
            numeric_limits<streamsize>::max(), '\n'
        );
        delete newNode;
        return;
    }

    newNode->next = NULL;
    newNode->prev = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        Node* temp = head;

        while (temp->next != NULL) {
            temp = temp->next;
        }

        temp->next = newNode;
        newNode->prev = temp;
    }

    cout << "Item added successfully!\n";
}

// Display grocery list
void displayList() {
    if (head == NULL) {
        cout << "Grocery list is empty.\n";
        return;
    }

    Node* temp = head;

    cout << "\n--- Grocery List ---\n";

    while (temp != NULL) {
        cout << "Item: " << temp->name
             << " | Quantity: " << temp->quantity
             << endl;

        temp = temp->next;
    }
}

// Search for an item
void searchItem() {
    string item;

    cout << "Enter item to search: ";
    cin >> ws;
    getline(cin, item);

    Node* temp = head;

    while (temp != NULL) {
        if (temp->name == item) {
            cout << "Item found! Quantity: "
                 << temp->quantity << endl;
            return;
        }

        temp = temp->next;
    }

    cout << "Item not found.\n";
}

// Update item quantity
void updateItem() {
    string item;

    cout << "Enter item to update: ";
    cin >> ws;
    getline(cin, item);

    Node* temp = head;

    while (temp != NULL) {
        if (temp->name == item) {
            int newQuantity;

            cout << "Enter new quantity: ";

            if (!(cin >> newQuantity) ||
                newQuantity <= 0) {
                cout << "Invalid quantity!\n";
                cin.clear();
                cin.ignore(
                    numeric_limits<streamsize>::max(),
                    '\n'
                );
                return;
            }

            temp->quantity = newQuantity;

            cout << "Quantity updated successfully!\n";
            return;
        }

        temp = temp->next;
    }

    cout << "Item not found.\n";
}

// Delete an item
void deleteItem() {
    string item;

    cout << "Enter item to delete: ";
    cin >> ws;
    getline(cin, item);

    Node* temp = head;

    while (temp != NULL) {
        if (temp->name == item) {

            // If deleting the first node
            if (temp->prev == NULL) {
                head = temp->next;
            } else {
                temp->prev->next = temp->next;
            }

            // If deleting the last node
            if (temp->next != NULL) {
                temp->next->prev = temp->prev;
            }

            delete temp;

            cout << "Item deleted successfully!\n";
            return;
        }

        temp = temp->next;
    }

    cout << "Item not found.\n";
}

// Free all allocated memory
void clearList() {
    while (head != NULL) {
        Node* temp = head;
        head = head->next;
        delete temp;
    }
}

// Main function
int main() {
    int choice;

    do {
        cout << "\n===== Grocery List System =====\n";
        cout << "1. Add Item\n";
        cout << "2. Display List\n";
        cout << "3. Search Item\n";
        cout << "4. Update Quantity\n";
        cout << "5. Delete Item\n";
        cout << "6. Exit\n";
        cout << "Enter your choice: ";

        if (!(cin >> choice)) {
            cout << "Invalid input! Enter a number.\n";
            cin.clear();
            cin.ignore(
                numeric_limits<streamsize>::max(), '\n'
            );
            continue;
        }

        switch (choice) {
            case 1:
                addItem();
                break;

            case 2:
                displayList();
                break;

            case 3:
                searchItem();
                break;

            case 4:
                updateItem();
                break;

            case 5:
                deleteItem();
                break;

            case 6:
                cout << "Exiting program.\n";
                break;

            default:
                cout << "Invalid choice!\n";
        }

    } while (choice != 6);

    clearList();

    return 0;
}
