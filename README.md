[practical 1.cpp](https://github.com/user-attachments/files/23619483/practical.1.cpp)
#include<stdio.h>

int main()
{
	int n,i,j,a[10];
	printf("enter the number of array you want:");
	scanf("%d",&n);
	
	for(int i=0;i<n;i++)
	{
		printf("\na[%d] = ",i);
		scanf("%d",&a[i]);
	}
	printf("\nyour array is:");
	for(int i=0;i<n;i++)
	{
		printf("\na[%d]=%d",i,a[i]);
	}
	printf("\n inerting elments in the array:");
	int num,pos;
	
	printf("\nenter the elemnts you want to enter in the array:");
	scanf("%d",&num);
	printf("\nenter the elment's positions:");
	scanf("%d",&pos);
    
	for(i=n-1;i>=pos;i--)
		a[i+1]=a[i];
		a[pos]=num;
	n=n+1;
	printf("\nyour array is:");
	for(int i=0;i<n;i++)
	{
		printf("\na[%d]=%d",i,a[i]);
	}
	
	//sorting the number:
	for(i=0;i<n-i;i++)
	{
		for(j=0;j<n-i-1;j++)
		{
			if (a[j] > a[j + 1])
			{
			int temp=a[j];
			a[j]=a[j+1];
		    a[j+1]=temp;
		    }
		}
	}
	printf("\nyour array is:");
	for(int i=0;i<n;i++)
	{
		printf("\na[%d]=%d",i,a[i]);
	}
    //cheak the duplicate number
	int flag=1;
	for(i=0;i<n;i++)
	{
	    for(j=i+1;j<n;j++)
		{
			if(a[i]==a[j] && i!=j)
		    {
			   printf("\n the duplicate number is %d & %d found at %d & %d",a[i],a[j],i,j);
			   //delete the duplicate number:
			   for(int k=j;k<=j;k++)
			   a[k]=a[k+1];
			   flag=0;
			   break;
			}
		}	
    n--;
	}
	
	if(flag==1)
	{
	   printf("\n no duplicate number found:");	
    }	
    else
	{
	printf("\nyour array is:");
	for(int i=0;i<n;i++)
	{
		printf("\na[%d]=%d",i,a[i]);
	}
    }
	
	return 0;
}
