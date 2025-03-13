#include<iostream>
using namespace std;
void insertionsort(int arr[],int n)
{
    int comparison=0;
    int shifting=0;
    for(int i=0;i<n;i++)
    {
        int key=arr[i];
        int j=i-1;
        
        while(j>=0 && arr[j]>key)
        {
            comparison++;
            arr[j+1]=arr[j];
            j=j-1;
             shifting++;
        }
        
        arr[j+1]=key;
shifting++;
    }
    
    cout<<"total comparison"<<comparison<<endl;
    cout<<"total shiifts"<<shifting<<endl;
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
    
    insertionsort(arr,n);
    
    cout<<"After insertion sort:"<<" ";
    for(int i=0;i<n;i++)
    {
        cout<<arr[i]<<" ";
    }
}
