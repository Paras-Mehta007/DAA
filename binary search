// Without recursion
#include<iostream>
using namespace std;

int main()
{
    int n,key;
    printf("enter the value of n:");
    scanf("%d",&n);
    
    int arr[100];
    
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }    
    printf(" enter the key to be seached:");
    scanf("%d",&key);
    
    int start=0;
    int  end=n-1;
    
    int flag=0;
    
    while(start<=end){
        
        int mid=start+(end-start)/2;
        
        if(arr[mid]==key)
        {
            printf("key found %d",mid);
            flag=1;
            
            break;
        }
        else if(arr[mid]>key)
        {
            end=mid-1;
        }
        else
        {
        start=mid+1;
    }
    }    
    if(flag==0)
    {
        printf("key not found");
    }
    return 0;
}


// with recursion

#include<iostream>
using namespace std;

void binarySearch(int arr[],int start,int end,int key)
{
    
    if(start>end) return;
    
    int mid=start+(end-start)/2;
    
    if(arr[mid]==key)
    {
        printf("key found %d",mid);
        return;
    }
    
    binarySearch(arr,mid+1,end,key);
     binarySearch(arr,start,mid-1,key);
}

int main()
{
    int n,key;
    printf("enter the value of n:");
    scanf("%d",&n);
    
    
    int arr[100];
    
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    
    printf(" enter the key to be seached:");
    scanf("%d",&key);
    
    binarySearch(arr,0,n-1,key);
    return 0;
}
