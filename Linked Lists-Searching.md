```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
void insertEnd(int);
void Search(int);

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
    Search(d);
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
void Search(int x){
    if(head!=NULL){
        struct Linkedlist *p=head;
        while(p!=NULL){
            if(x==p->data){
                printf("yes");
                return;
            }
            p=p->next;
        }
    }
    printf("no");
}
```
