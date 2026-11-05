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

    first->data = 10;
    second->data = 20;
    third->data = 30;
    fourth->data = 40;
    fifth->data = 50;

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
    newNode->data = 5;
    newNode->prev = nullptr;
    newNode->next = head;

    head->prev = newNode;
    head = newNode;

    newNode = new Node();
    newNode->data = 25;

    newNode->prev = second;
    newNode->next = second->next;

    second->next->prev = newNode;
    second->next = newNode;

    newNode = new Node();
    newNode->data = 60;
    newNode->next = nullptr;
    newNode->prev = tail;

    tail->next = newNode;
    tail = newNode;

    Node* temp = head;

    while (temp != nullptr)
    {
        cout << temp->data << " ";
        temp = temp->next;
    }

    return 0;
}
