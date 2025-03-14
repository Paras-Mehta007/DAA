#include<iostream>
#include<vector>
using namespace std;

void merge(vector<int>&arr,int mid,int low,int high)
{
    int temp[high-low+1];
    int left=low;
    int right=mid+1;

    int i=0;
    while(left<=mid && right<=high)
    {
        if(arr[left]<=arr[right])
        {
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

    for(int i=low;i<=high;i++){
        arr[i]=temp[i-low];
    }
}


void mergesort(vector<int>&arr,int low,int high)
{
    if(low>=high)
    {
        return;
    }
    int mid=low+(high-low)/2;
    mergesort(arr,low,mid);
    mergesort(arr,mid+1,high);
    merge(arr,mid,low,high);
}
void sum(vector<int>&arr,int key)
{
    int n=arr.size();
    mergesort(arr,0,n-1);

  int i=0;
  int j=n-1;
  int flag=0;
  while(i<j)
  {
    int sum=arr[i]+arr[j];
    if(sum==key)
    {
        cout<<arr[i]<<","<<arr[j]<<endl;;
        flag=1;
        break;
    }
    else if(sum<key)
    {
        i++;
    }else{
        j--;
    }
  }

  if(flag==0)
  {
    cout<<"No such element exist"<<endl;
  }

}
int main()
{
    int n;
    cout<<"enter the size of the array:";
    cin >> n;

    vector<int>arr(n);
    cout<<"enter the elements of the Array:";
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }

    int key;
    cout<<"enter the key :";
    cin>>key;

     sum(arr,key);

     for(int i=0;i<n;i++)
     {
        cout<<arr[i]<<" ";
     }

    
}
