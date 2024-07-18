#include<stdio.h>
#include<stdlib.h>
struct it
{
    int data;
    struct it *next;
};
struct it *head=NULL;
struct it *temp;

int create(int x){
    struct it newnode = (struct it)malloc(sizeof(struct it));
    newnode->data = x;
    newnode->next = NULL;
    if(head == NULL){
        head = newnode;
    }
    else{
        temp = head;
        while(temp->next!=NULL){
            temp = temp->next;
        }
        temp->next = newnode;
    }
}

int display(){
    int sum=0;
    temp = head;
    while(temp!=NULL){
        printf("%d ",temp->data);
        temp=temp->next;
    }
    printf("\n%d\n%d\n%d",sum);
}

int eve_odd()
{
    int es=0,os=0;
    temp = head;
    while(temp!=NULL){
        if(temp->data%2==0){
            es=es+temp->data;
            temp=temp->next;
        }
        else
        {
            os=os+temp->data;
            temp=temp->next;
        }
        printf("%d\n",es);
          printf("%d",os);
    }
}

int search()
{
    
}
int main()
{
    create(10);
    create(20);
    create(30);
    create(40);
    display();
    eve_odd();
    
}
