#include<stdio.h>
#include<stdlib.h>
int binarySearch(int *a,int low,int high,int key)
{
   int i,mid;
   while(low<=high)
   {
       mid=(low+high)/2;
       if(key==a[mid])
      return mid;//return mid+1(for postions)
       if(key<a[mid])
       high=mid-1;
       else//serach on right side low=mid+1
      low=mid+1;
   }
   return -1;
}
int main()
{
    int *a,n,i,t,key;
    scanf("%d",&n);
    a=(int *)malloc(n*sizeof(int));
    for(i=0;i<n;i++)
    scanf("%d",&a[i]);
    scanf("%d",&key);
   t=binarySearch(a,0,n-1,key);
    printf("%d ",t);
    return 0;
}
