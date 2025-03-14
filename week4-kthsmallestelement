#include <iostream>
#include<vector>
using namespace std; 

int partition(vector<int>&arr,int left ,int right){

    int pivot=arr[left];
    int i=left+1;
    int j=right;

    while(i <= j)
    {
        while(i <= right && arr[i] <= pivot) i++; // Move i right until we find a larger element
        while(j >= left && arr[j] > pivot) j--;  // Move j left until we find a smaller element
        
        if(i < j) {
            swap(arr[i], arr[j]);
        }
    }
    swap(arr[left], arr[j]);
    return j;
}

int findkthSmallest(vector<int>&arr,int k)
{
    int n=arr.size();
    int left=0;
    int right=n-1;

    int pivot_idx=0;

    while(true)
    {
        pivot_idx=partition(arr,left,right);

        if(pivot_idx == k-1)
        {
            break;
        }else if(pivot_idx>k-1)
        {
            right=pivot_idx-1;
        }else{
            left=pivot_idx+1;
        }
    }
    return arr[pivot_idx];
}

int main()
{
    int n;
    cout<<"enter the Size of the Array:";
    cin>>n;

    vector<int>arr(n);
    cout<<"enter the elements of the Array:"; 
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }

    int k;
    cout<<"enter the kth smallest element:";
    cin>>k;

    int kthsmallest=findkthSmallest(arr,k);

    cout<<"kth smallest element is:"<<kthsmallest<<endl;
}
