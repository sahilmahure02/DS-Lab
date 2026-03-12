#include <stdio.h> printf("Number %d not found\n", num); return; }

if (temp == head) {
    head = temp->next;
    if (head != NULL)
        head->prev = NULL;
} else {
    temp->prev->next = temp->next;
    if (temp->next != NULL)
        temp->next->prev = temp->prev;
}

free(temp);

printf("List after deletion: ");
display();
}

// Function to reverse the list void reverseList() { if (head == NULL) { printf("List is empty\n"); return; }

struct Node *temp = NULL;
struct Node *current = head;

while (current != NULL) {
    temp = current->prev;
    current->prev = current->next;
    current->next = temp;
    current = current->prev;
}

if (temp != NULL)
    head = temp->prev;

display();
}

// Function to concatenate another list void concatenate() { int n; scanf("%d", &n);

if (n == 0) {
    printf("Second list is empty\n");
    return;
}

struct Node* tail = head;
