#include <iostream>
using namespace std;

class Node
{
public:
    int data;
    Node* next;

    Node(int value)
    {
        data = value;
        next = NULL;
    }
};

class LinkedList
{
public:
    Node* head;

    LinkedList()
    {
        head = NULL;
    }

    void insertAtEnd(int value)
    {
        Node* newNode = new Node(value);

        if (head == NULL)
        {
            head = newNode;
            return;
        }

        Node* temp = head;

        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        temp->next = newNode;
    }

    void deleteByValue(int value)
    {
        // Case 1: List is empty
        if (head == NULL)
        {
            cout << "Value not found" << endl;
            return;
        }

        // Case 2: Value is in the first node
        if (head->data == value)
        {
            Node* temp = head;
            head = head->next;
            delete temp;
            return;
        }

        Node* temp = head;

        while (temp->next != NULL && temp->next->data != value)
        {
            temp = temp->next;
        }

        if (temp->next == NULL)
        {
            cout << "Value not found" << endl;
            return;
        }

        // Delete the node
        Node* nodeToDelete = temp->next;

        temp->next = nodeToDelete->next;

        delete nodeToDelete;
    }

    void display()
    {
        Node* temp = head;

        while (temp != NULL)
        {
            cout << temp->data;

            if (temp->next != NULL)
                cout << " -> ";

            temp = temp->next;
        }

        cout << endl;
    }
};

int main()
{
    LinkedList list;

    list.insertAtEnd(10);
    list.insertAtEnd(20);
    list.insertAtEnd(30);
    list.insertAtEnd(40);
    list.insertAtEnd(50);

    cout << "Original List: ";
    list.display();

    // Delete first node
    list.deleteByValue(10);

    cout << "After deleting 10: ";
    list.display();

    // Delete middle node
    list.deleteByValue(30);

    cout << "After deleting 30: ";
    list.display();

    // Delete last node
    list.deleteByValue(50);

    cout << "After deleting 50: ";
    list.display();

    // Value does not exist
    list.deleteByValue(100);

    cout << "Final List: ";
    list.display();

    return 0;
}
