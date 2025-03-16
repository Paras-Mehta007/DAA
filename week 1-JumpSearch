#include<iostream>
#include<cmath>
using namespace std;

int jumpsearch(vector<int>&arr,int n,int key)
{
    int start=0,end=sqrt(n);

    while(arr[end]<=key && end<n)
    {
        start=end;
        end+=sqrt(n);
        if(end>n) end=n;
    }
    for(int i=start;i<end;i++)
    {
        if(arr[i]==key)
        return i;

    }

    return -1;

}

int main()
{
    int n;
    cout<<"enter the size of the Array:";
    cin>>n;

    vector<int>arr(n);
    cout<<"enter the elements of the array:";
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }

    int key;
    cout<<"enter the elements to be searched:";
    cin>>key;

    int index=jumpsearch(arr,n,key);

    if(index!=-1)
    {
        cout<<"Element found at index:"<<index;
    }else
    {
        cout<<"Not Found";
    }

    return 0;
}
