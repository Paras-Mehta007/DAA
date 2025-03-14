#include <iostream>
#include<vector>
using namespace std; 

int partition(vector<int>&arr,int left ,int right){

    int pivot=arr[left];
    int i=left+1;
    int j=right;

    while(i<=j)
    {
        if(arr[i]<pivot && arr[j]>pivot){
            swap(arr[i],arr[j]);
            i++;
            j--;    
        }
        if(arr[i]>=pivot){
            i++;
        }

        if(arr[j]<=pivot){
            j--;
        }
    }
    swap(arr[left],arr[j]);
    return j;
}

int findkthLargest(vector<int>&arr,int k)
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
    cout<<"enter the kth largest element:";
    cin>>k;

    int kthlargest=findkthLargest(arr,k);

    cout<<"kth largest element is:"<<kthlargest<<endl;
}
