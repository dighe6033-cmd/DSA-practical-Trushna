#include <iostream>
#include <string>
using namespace std;

struct Node {
    string name;
    int quantity;
    Node* next;
};

Node* head = NULL;

// Add grocery item
void addItem() {
    Node* newNode = new Node;
    cout << "Enter item name: ";
    cin >> ws;
    getline(cin, newNode->name);

    cout << "Enter quantity: ";
    cin >> newNode->quantity;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        Node* temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newNode;
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
             << " | Quantity: " << temp->quantity << endl;
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
            cout << "Enter new quantity: ";
            cin >> temp->quantity;
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
    Node* prev = NULL;

    while (temp != NULL) {
        if (temp->name == item) {
            if (prev == NULL)
                head = temp->next;
            else
                prev->next = temp->next;

            delete temp;
            cout << "Item deleted successfully!\n";
            return;
        }
        prev = temp;
        temp = temp->next;
    }
#include <iostream>
#include <string>
using namespace std;

struct Node {
    string name;
    int quantity;
    Node* next;
};

Node* head = NULL;

// Add grocery item
void addItem() {
    Node* newNode = new Node;
    cout << "Enter item name: ";
    cin >> ws;
    getline(cin, newNode->name);

    cout << "Enter quantity: ";
    cin >> newNode->quantity;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        Node* temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newNode;
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
             << " | Quantity: " << temp->quantity << endl;
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
            cout << "Enter new quantity: ";
            cin >> temp->quantity;
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
    Node* prev = NULL;

    while (temp != NULL) {
        if (temp->name == item) {
            if (prev == NULL)
                head = temp->next;
            else
                prev->next = temp->next;

            delete temp;
            cout << "Item deleted successfully!\n";
            return;
        }
        prev = temp;
        temp = temp->next;
    }
    cout << "Item not found.\n";
}

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
        cin >> choice;

        switch (choice) {
            case 1: addItem(); break;
            case 2: displayList(); break;
            case 3: searchItem(); break;
            case 4: updateItem(); break;
            case 5: deleteItem(); break;
            case 6: cout << "Exiting program.\n"; break;
            default: cout << "Invalid choice!\n";
        }
    } while (choice != 6);

    while (head != NULL) {
        Node* temp = head;
        head = head->next;
        delete temp;
    }

    return 0;
}#include <iostream>
#include <string>
using namespace std;

struct Node {
    string name;
    int quantity;
    Node* next;
};

Node* head = NULL;

// Add grocery item
void addItem() {
    Node* newNode = new Node;
    cout << "Enter item name: ";
    cin >> ws;
    getline(cin, newNode->name);

    cout << "Enter quantity: ";
    cin >> newNode->quantity;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        Node* temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newNode;
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
             << " | Quantity: " << temp->quantity << endl;
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
            cout << "Enter new quantity: ";
            cin >> temp->quantity;
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
    Node* prev = NULL;

    while (temp != NULL) {
        if (temp->name == item) {
            if (prev == NULL)
                head = temp->next;
            else
                prev->next = temp->next;
#include <iostream>
#include <string>
using namespace std;

struct Node {
    string name;
    int quantity;
    Node* next;
};

Node* head = NULL;

// Add grocery item
void addItem() {
    Node* newNode = new Node;
    cout << "Enter item name: ";
    cin >> ws;
    getline(cin, newNode->name);

    cout << "Enter quantity: ";
    cin >> newNode->quantity;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        Node* temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newNode;
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
             << " | Quantity: " << temp->quantity << endl;
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
            cout << "Enter new quantity: ";
            cin >> temp->quantity;
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
    Node* prev = NULL;

    while (temp != NULL) {
        if (temp->name == item) {
            if (prev == NULL)
                head = temp->next;
            else
                prev->next = temp->next;

            delete temp;
            cout << "Item deleted successfully!\n";
            return;
        }
        prev = temp;
        temp = temp->next;
    }
    cout << "Item not found.\n";
}

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
        cin >> choice;

        switch (choice) {
            case 1: addItem(); break;
            case 2: displayList(); break;
            case 3: searchItem(); break;
            case 4: updateItem(); break;
            case 5: deleteItem(); break;
            case 6: cout << "Exiting program.\n"; break;
            default: cout << "Invalid choice!\n";
        }
    } while (choice != 6);

    while (head != NULL) {
        Node* temp = head;
        head = head->next;
        delete temp;
    }

    return 0;
}#include <iostream>
#include <string>
using namespace std;

struct Node {
    string name;
    int quantity;
    Node* next;
};

Node* head = NULL;

// Add grocery item
void addItem() {
    Node* newNode = new Node;
    cout << "Enter item name: ";
    cin >> ws;
    getline(cin, newNode->name);

    cout << "Enter quantity: ";
    cin >> newNode->quantity;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        Node* temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newNode;
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
             << " | Quantity: " << temp->quantity << endl;
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
            cout << "Enter new quantity: ";
            cin >> temp->quantity;
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
    Node* prev = NULL;

    while (temp != NULL) {
        if (temp->name == item) {
            if (prev == NULL)
                head = temp->next;
            else
                prev->next = temp->next;

            delete temp;
            cout << "Item deleted successfully!\n";
            return;
        }
        prev = temp;
        temp = temp->next;
    }
    cout << "Item not found.\n";
}

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
        cin >> choice;

        switch (choice) {
            case 1: addItem(); break;
            case 2: displayList(); break;
            case 3: searchItem(); break;
            case 4: updateItem(); break;
            case 5: deleteItem(); break;
            case 6: cout << "Exiting program.\n"; break;
            default: cout << "Invalid choice!\n";
        }
    } while (choice != 6);

    while (head != NULL) {
        Node* temp = head;
        head = head->next;
        delete temp;
    }

    return 0;
}#include <iostream>
#include <string>
using namespace std;

struct Node {
    string name;
    int quantity;
    Node* next;
};

Node* head = NULL;

// Add grocery item
void addItem() {
    Node* newNode = new Node;
    cout << "Enter item name: ";
    cin >> ws;
    getline(cin, newNode->name);

    cout << "Enter quantity: ";
    cin >> newNode->quantity;
    newNode->next = NULL;

    if (head == NULL) {
        head = newNode;
    } else {
        Node* temp = head;
        while (temp->next != NULL)
            temp = temp->next;
        temp->next = newNode;
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
             << " | Quantity: " << temp->quantity << endl;
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
            cout << "Enter new quantity: ";
            cin >> temp->quantity;
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
    Node* prev = NULL;

    while (temp != NULL) {
        if (temp->name == item) {
            if (prev == NULL)
                head = temp->next;
            else
                prev->next = temp->next;

            delete temp;
            cout << "Item deleted successfully!\n";
            return;
        }
        prev = temp;
        temp = temp->next;
    }
    cout << "Item not found.\n";
}

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
        cin >> choice;

        switch (choice) {
            case 1: addItem(); break;
            case 2: displayList(); break;
            case 3: searchItem(); break;
            case 4: updateItem(); break;
            case 5: deleteItem(); break;
            case 6: cout << "Exiting program.\n"; break;
            default: cout << "Invalid choice!\n";
        }
    } while (choice != 6);

    while (head != NULL) {
        Node* temp = head;
        head = head->next;
        delete temp;
    }

    return 0;
}
