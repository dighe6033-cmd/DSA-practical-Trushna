## Code: 

#include <iostream>
using namespace std;

struct Node
{
    int rollNo;
    Node* left;
    Node* right;
};

Node* createNode(int rollNo)
{
    Node* newNode = new Node;
    newNode->rollNo = rollNo;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}

Node* insert(Node* root, int rollNo)
{
    if (root == NULL)
        return createNode(rollNo);

    if (rollNo < root->rollNo)
        root->left = insert(root->left, rollNo);
    else if (rollNo > root->rollNo)
        root->right = insert(root->right, rollNo);
    else
        cout << "Roll number already exists!\n";

    return root;
}

bool search(Node* root, int rollNo)
{
    if (root == NULL)
        return false;

    if (root->rollNo == rollNo)
        return true;

    if (rollNo < root->rollNo)
        return search(root->left, rollNo);

    return search(root->right, rollNo);
}

void inorder(Node* root)
{
    if (root != NULL)
    {
        inorder(root->left);
        cout << root->rollNo << " ";
        inorder(root->right);
    }
}

int main()
{
    Node* root = NULL;
    int choice, rollNo;

    do
    {
        cout << "\n\n--- Student Roll Number Management ---\n";
        cout << "1. Insert Roll Number\n";
        cout << "2. Search Roll Number\n";
        cout << "3. Display Roll Numbers\n";
        cout << "4. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice)
        {
            case 1:
                cout << "Enter roll number: ";
                cin >> rollNo;
                root = insert(root, rollNo);
                cout << "Roll number inserted successfully.\n";
                break;

            case 2:
                cout << "Enter roll number to search: ";
                cin >> rollNo;

                if (search(root, rollNo))
                    cout << "Roll number found!\n";
                else
                    cout << "Roll number not found!\n";
                break;

            case 3:
                cout << "Student Roll Numbers: ";
                inorder(root);
                cout << endl;
                break;

            case 4:
                cout << "Exiting program...\n";
                break;

            default:
                cout << "Invalid choice! Try again.\n";
        }

    } while (choice != 4);
    return 0;
}

    return 0;
}
