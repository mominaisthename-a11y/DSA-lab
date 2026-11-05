#include <iostream>
using namespace std;

struct Node
{
    int data;
    Node* prev;
    Node* next;
};

int main()
{
    Node* first = new Node();
    Node* second = new Node();
    Node* third = new Node();
    Node* fourth = new Node();
    Node* fifth = new Node();

    first->data = 101;
    second->data = 102;
    third->data = 103;
    fourth->data = 104;
    fifth->data = 105;

    first->prev = nullptr;
    first->next = second;

    second->prev = first;
    second->next = third;

    third->prev = second;
    third->next = fourth;

    fourth->prev = third;
    fourth->next = fifth;

    fifth->prev = fourth;
    fifth->next = nullptr;

    Node* head = first;
    Node* tail = fifth;

    Node* newNode = new Node();
    newNode->data = 100;
    newNode->prev = nullptr;
    newNode->next = head;

    head->prev = newNode;
    head = newNode;

    newNode = new Node();
    newNode->data = 1035;

    newNode->prev = third;
    newNode->next = third->next;

    third->next->prev = newNode;
    third->next = newNode;

    newNode = new Node();
    newNode->data = 106;
    newNode->next = nullptr;
    newNode->prev = tail;

    tail->next = newNode;
    tail = newNode;

    Node* temp = head;
    head = head->next;
    head->prev = nullptr;
    delete temp;

    temp = fourth;

    temp->prev->next = temp->next;
    temp->next->prev = temp->prev;

    delete temp;

    temp = tail;
    tail = tail->prev;
    tail->next = nullptr;

    delete temp;

    temp = head;

    while (temp != nullptr)
    {
        cout << temp->data << " ";
        temp = temp->next;
    }

    return 0;
}
