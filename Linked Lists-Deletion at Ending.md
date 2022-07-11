# Linked Lists-Deletion at Ending
Write a program to create a linked list with the given number of elements(follow the normal insertion process i.e., insert node at end evry time).
If there are no elements given then the head of the linked list will be null. After completing the insertion of all you will be given a value of "k". 
  Perform the deletion at ending k times. Print the elements in the linked list after successful completion of deletion.

Note: Intially the linked list will be empty. The k value always will be less than no.of elements in the list <br/>
**Input Format**<br />
``
First Line contains number of elements(n) to be inserted and followed the n+1 elements the (n+1)th element denotes k value.
``
**Constraints** <br />

0<=n<=100 <br/>
1<=element<=10000 <br/>
0<=k<=1000
<br/>

**Output Format**
```
Print the elements in the linked list.
```
**Sample Input 0**
```
4
1
2
3
4
2
```
**Sample Output 0**
```
1->2
```

### Solution (C)
```c
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
void insertEnd(int);
void Display();
void delete();

struct Linkedlist{
    int data;
    struct Linkedlist *next;
};
struct Linkedlist *head=NULL;
int main() {
    int n,i,x,d;
    scanf("%d",&n);
    for(i=0;i<n;i++){
        scanf("%d",&x);
        insertEnd(x);
    }
    scanf("%d",&d);
    while(d--)
    delete();
    Display();
    return 0;
}
void insertEnd(int data){
    struct Linkedlist *New = (struct Linkedlist*)malloc(sizeof(struct Linkedlist));
    New->data=data;
    New->next=NULL;
    if(head==NULL)
        head=New;
    else{
    struct Linkedlist *p=head;
    while(p->next!=NULL){
        p=p->next;
    }
    p->next=New;
    }
}
void delete(){
    if(head==NULL) return;
    else if(head->next==NULL){
        struct Linkedlist *t=head;
        head=head->next;
        free(t);
    }
    else{
        struct Linkedlist *temp=head;
        while(temp->next->next)
            temp=temp->next;
        struct Linkedlist *t=temp->next;
        temp->next=NULL;
        free(t);
    }
}
void Display(){
    if(head!=NULL){
        struct Linkedlist *p=head;
        while(p->next!=NULL){
            printf("%d->",p->data);
            p=p->next;
        }
        printf("%d",p->data);
    }
}

```
