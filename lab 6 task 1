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

    void deleteAtStart()
    {
        if (head == NULL)
        {
            cout << "List is empty" << endl;
            return;
        }

        Node* temp = head;
        head = head->next;
        delete temp;
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

    list.deleteAtStart();

    cout << "After first deletion: ";
    list.display();

    list.deleteAtStart();

    cout << "After second deletion: ";
    list.display();

    return 0;
}
