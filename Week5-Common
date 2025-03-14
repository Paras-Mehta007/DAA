#include<iostream>
#include<vector>
using namespace std;

void Common(int arr[],int brr[],int n,int m,vector<int>&ans)
{
    int i=0;
    int j=0;
    int flag=0;

    while(i<n && j<m)
    {
        if(arr[i]==brr[j])
        {
          ans.push_back(arr[i]);
          i++;
          j++;
          flag=1;
        }else if(arr[i]<brr[j]){
            i++;
        }else{
            j++;
        }
    }

    if(flag==0)
    {
      cout<<"No element Common";
    }
}

int main()
{
    int n;
    cout<<"enter the size of the first Array:";
    cin>>n;
    
    int m;
    cout<<"enter the size of the second Array:";
    cin>>m;

    int arr[n];
    cout<<"enter the elements of First array:";
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
    }
    int brr[m];
    cout<<"enter the elements of the second array:";
    for(int i=0;i<m;i++)
    {
        cin>>brr[i];
    }
    vector<int>ans(0);

    Common(arr,brr,n,m,ans);

    for(int i=0;i<ans.size();i++)
    {
        cout<<ans[i]<<" ";
    }

}
