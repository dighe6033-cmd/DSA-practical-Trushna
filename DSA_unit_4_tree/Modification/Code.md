## Code:

#include <iostream>
#include <string>
using namespace std;

struct Node
{
    int rollNo;
    string name;
    Node* left;
    Node* right;
};

Node* createNode(int rollNo, string name)
{
    Node* newNode = new Node;
    newNode->rollNo = rollNo;
    newNode->name = name;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}

// Insert student record
Node* insert(Node* root, int rollNo, string name)
{
    if (root == NULL)
        return createNode(rollNo, name);

    if (rollNo < root->rollNo)
        root->left = insert(root->left, rollNo, name);
    else if (rollNo > root->rollNo)
        root->right = insert(root->right, rollNo, name);
    else
        cout << "Roll number already exists!\n";

    return root;
}

// Search student record
Node* search(Node* root, int rollNo)
{
    if (root == NULL || root->rollNo == rollNo)
        return root;

    if (rollNo < root->rollNo)
        return search(root->left, rollNo);

    return search(root->right, rollNo);
}

// Find minimum node
Node* findMin(Node* root)
{
    while (root != NULL && root->left != NULL)
        root = root->left;

    return root;
}

// Delete student record
Node* deleteNode(Node* root, int rollNo)
{
    if (root == NULL)
        return root;

    if (rollNo < root->rollNo)
        root->left = deleteNode(root->left, rollNo);
    else if (rollNo > root->rollNo)
        root->right = deleteNode(root->right, rollNo);
    else
    {
        if (root->left == NULL)
        {
            Node* temp = root->right;
            delete root;
            return temp;
        }
        else if (root->right == NULL)
        {
            Node* temp = root->left;
            delete root;
            return temp;
        }

        Node* temp = findMin(root->right);

        root->rollNo = temp->rollNo;
        root->name = temp->name;

        root->right = deleteNode(root->right,
                                 temp->rollNo);
    }

    return root;
}

// Update student name
void update(Node* root, int rollNo)
{
    Node* temp = search(root, rollNo);

    if (temp == NULL)
        cout << "Student record not found!\n";
    else
    {
        cout << "Enter new student name: ";
        getline(cin >> ws, temp->name);

        cout << "Student record updated successfully!\n";
    }
}

// Display records in ascending order
void inorder(Node* root)
{
    if (root != NULL)
    {
        inorder(root->left);

        cout << "Roll Number: " << root->rollNo
             << " | Name: " << root->name << endl;

        inorder(root->right);
    }
}

int main()
{
    Node* root = NULL;
    int choice, rollNo;
    string name;

    do
    {
        cout << "\n--- Student Roll Number Management ---\n";
        cout << "1. Insert Student\n";
        cout << "2. Search Student\n";
        cout << "3. Update Student\n";
        cout << "4. Delete Student\n";
        cout << "5. Display Students\n";
        cout << "6. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice)
        {
            case 1:
                cout << "Enter roll number: ";
                cin >> rollNo;

                cout << "Enter student name: ";
                getline(cin >> ws, name);

                if (search(root, rollNo) != NULL)
                    cout << "Roll number already exists!\n";
                else
                {
                    root = insert(root, rollNo, name);
                    cout << "Student inserted successfully!\n";
                }
                break;

            case 2:
                cout << "Enter roll number to search: ";
                cin >> rollNo;

                {
                    Node* temp = search(root, rollNo);

                    if (temp != NULL)
                    {
                        cout << "Student Found!\n";
                        cout << "Roll Number: "
                             << temp->rollNo << endl;
                        cout << "Name: "
                             << temp->name << endl;
                    }
                    else
                        cout << "Student record not found!\n";
                }
                break;

            case 3:
                cout << "Enter roll number to update: ";
                cin >> rollNo;
                update(root, rollNo);
                break;

            case 4:
                cout << "Enter roll number to delete: ";
                cin >> rollNo;

                if (search(root, rollNo) != NULL)
                {
                    root = deleteNode(root, rollNo);
                    cout << "Student deleted successfully!\n";
                }
                else
                    cout << "Student record not found!\n";

                break;

            case 5:
                if (root == NULL)
                    cout << "No student records available.\n";
                else
                {
                    cout << "\nStudent Records "
                         << "in Ascending Order:\n";
                    inorder(root);
                }
                break;

            case 6:
                cout << "Exiting program...\n";
                break;

            default:
                cout << "Invalid choice! Try again.\n";
        }

    } while (choice != 6);

    return 0;
}
