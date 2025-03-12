#include<iostream>
#include<vector>
using namespace std;

void difference(vector<int>&arr,int n,int key)
{
    int count=0;

    for(int i=0;i<n;i++)
    {
        for(int j=i+1;j<n;j++)
        {
            if(arr[i]-arr[j]==key || arr[j]-arr[i]==key)
            {
                count++;
            }
        }
    }

    if(count!=0)
    {
        cout<<"pairs are "<<count;
    }
    else{
        cout<<"no pairs found";
    }
}
int main(){
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
        cout<<"enter the key";
        cin>>key;
    
    difference(arr,n,key);
}
