#include<stdio.h>
#include<stdlib.h>
void append();
void display();
struct node 
{
int data;
struct node *link;
};
struct node *root=NULL;
int main ()
{
	int ch;
	while(1)
	{
	
	printf("press 1 for append \n");
	printf("press 2 for display\n");
	printf("press 3 for exit \n");
	scanf("%d",&ch);
	switch (ch)
	{
		case 1:
			 append ();
			break;
			case 2:
				 display();
				break;
				case 3:
					exit(0);
					break;
						
		}
	}
		return 0;
}
void append ()
{
	struct node *temp = NULL;
	struct node *p = NULL;
	temp=(struct node*)malloc(sizeof(struct node));
	printf("enter the data :");
	scanf("%d",&temp->data);
	if(root==NULL)
	{
		root=temp;
	}
	else{
		p=root;
		while(p->link!=NULL)
		{
			p=p->link;
		}
		p->link=temp;
}
}
void display()
{
	struct node *temp=root;
	if(root==NULL)
	{
		printf("list is empty");
	}
	else {
		while (temp->link!=NULL)
		{
			printf("%d",temp->data);
			temp=temp->link;
		}
		printf("%d",temp->data);
	}
}


	
