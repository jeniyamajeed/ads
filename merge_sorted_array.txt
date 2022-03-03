#include <stdio.h>

void main()
{
  int a[10],b[10],c[20],i,j,k,n1,n2,temp;
  printf("enter the size of first array:");
  scanf("%d",&n1);
  printf("enter the array elements:");
  for(i=0;i<n1;i++)
  {
      scanf("%d",&a[i]);
     
  }
  printf("sorted array is:");
  for(i=0;i<n1;i++)
  {
      for(j=i;j<n1;j++)
      {
          if (a[i]>a[j])
          {
              temp=a[i];
              a[i]=a[j];
              a[j]=temp;
              
          }
      }
  }
  for(i=0;i<n1;i++)
  {
      printf("%d",a[i]);
      c[i]=a[i];
      
  }
  printf("\n");
  k=i;
  printf("enter the size of second array:");
  scanf("%d",&n2);
  printf("enter the array elements:");
  for(i=0;i<n2;i++)
  {
      scanf("%d",&b[i]);
     
  }
  printf("sorted array is:");
  for(i=0;i<n2;i++)
  {
      for(j=i+1;j<n2;j++)
      {
          if (b[i]>b[j])
          {
              temp=b[i];
              b[i]=b[j];
              b[j]=temp;
              
          }
      }
  }
  for(i=0;i<n2;i++)
  {
      printf("%d",b[i]);
      c[k]=b[i];
      k++;
      
  } 
  printf("\nmerged array is:");
  for(i=0;i<k;i++)
  {
      printf("%d\t",c[i]);
      
  }
}
