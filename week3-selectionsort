#include<iostream>
#include<algorithm>
using namespace std;

void selectionsort(int arr[],int n)
{
    int comparison=0;
    int noofswaps=0;
    
    for(int i=0;i<n-1;i++)
    {
        int minindx=i;
        
        for(int j=i+1;j<n;j++)
        {
            comparison++;
            if(arr[j]<arr[minindx])
            {
                minindx=j;
            }
        }
        
        swap(arr[i],arr[minindx]);
        noofswaps++;
    }
    cout<<"total no of comparison"<<comparison<<endl;
    cout<<"total no of swaps"<<noofswaps<<endl;
}

int main()
{
    int n;
    cout<<"enter the size of the araay";
    cin>>n;
    
    int arr[n];
    cout<<"enter the elment of the array:";
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }    
    selectionsort(arr,n);    
    cout<<"After insertion sort:"<<" ";
    for(int i=0;i<n;i++)
    {
        cout<<arr[i]<<" ";
    }
}
