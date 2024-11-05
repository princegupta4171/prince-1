# prince-1
This is my first Git Repository
<br>
<br>
Author-Prince Gupta internet
#include<stdio.h>
#include<stdlib.h>

struct node
{
 int data;
 struct node*next;
};

struct node*head=NULL;

void create();
void display();
int count();

int main()
{
 int x;
 create();
 display();
 x=count();
 printf("there are %d nodes",x);
 }
 
void create()
{
 int ch;
 struct node *ptr,*temp;
 do
 {
  ptr=(struct node *)malloc(sizeof(struct node));
  printf("enter the data part \n");
  printf("\t");
  scanf("%d",&ptr->data);
  if(head=NULL)
  {
   head=ptr;
   temp=ptr;
   }
  else
  {
   temp->next=ptr;
   temp=ptr;
   } 
  printf("do you want to continue \n press 1\n otherwise \n press 0");
  scanf("%d",&ch);
  }while(ch==1);
  ptr->next=NULL;
 }

void display()
{
 struct node*temp=head;
 while(temp!=NULL)
 {
  printf("%d \t",temp->data);
  temp=temp->next;
  }
 }
 
int count()
{
 int count =0;
 struct node*temp=head;
 while(temp!=NULL)
 {
  count++;
  temp=temp->next;
  }
  return count;
 }
 
 
