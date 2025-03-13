#include<iostream>
#include<vector>
using namespace std;

void merge(vector<int>&arr,int mid,int low,int high){
     int left=low;
     int right=mid+1;
    int temp[high-low+1];

    int i=0;
    while(left<=mid && right<=high){
     if(arr[left]<=arr[right]){
        temp[i++]=arr[left++];

     }else{
        temp[i++]=arr[right++];
     }
}

while(left<=mid)
{
    temp[i++]=arr[left++];
}

while(right<=high)
{
    temp[i++]=arr[right++];
}

 for(int i=low;i<=high;i++)
 {
    arr[i]=temp[i-low];
 }

}

void mergesort(vector<int>&arr,int start,int end){

    if(start>=end){
        return;
    }
    int mid=start+(end-start)/2;
    mergesort(arr,start,mid);
    mergesort(arr,mid+1,end);
    merge(arr,mid,start,end);
}

int main()
{
    int n;
    cout<<"Enter the size of the Array:";
    cin>>n;

    vector<int>arr(n);
    cout<<"Enter the elements of the Array:";
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }

    mergesort(arr,0,n-1);

    for(int i=0;i<n;i++)
    {
        cout<<arr[i]<<" ";
    }

    cout<<endl;


    int flag=0;
    for(int i=0;i<n-1;i++)
    {
        if(arr[i]==arr[i+1])
        {
            flag=1;
        }
    }

    if(flag!=0)
    {
        cout<<"yes";
    }
    else{
        cout<<"No";
    }
}
