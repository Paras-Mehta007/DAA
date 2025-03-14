#include<iostream>
#include<vector>
using namespace std;
char max_frequency_char='\0';
int max_freq=0;
bool duplicate=false;
void count_sort(char arr[],int n)
{
    // bool duplicate=false;
    int count[26];
    int brr[n];

    for(int i=0;i<26;i++)
    {
        count[i]=0;
    }

 for(int i=0;i<n;i++)
 {
    if(++count[arr[i]-'a']>1)
    {
        duplicate=true;
    }
    if(count[arr[i]-'a']>max_freq){
        max_freq=count[arr[i]-'a'];
        max_frequency_char=arr[i];
    }
 }

 for(int i=1;i<26;i++)
 {
    count[i]=count[i]+count[i-1];
 }

 for(int i=n-1;i>=0;i--)
 {
    brr[--count[arr[i]-'a']]=arr[i];
 }

 for(int i=0;i<n;i++)
 {
    arr[i]=brr[i];
 }

}

int main()
{
    int n;
    cout<<"enter the size of the array:";
    cin>>n;

   char arr[n];  
    cout<<"enter the elements of the array:"<<endl;
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    count_sort(arr,n);
    for(int i=0;i<n;i++)
    {
        cout<<arr[i]<<" ";
    }
    cout<<endl;

   if(duplicate!=false)
   {
    cout<<"Most frequent character :"<<max_frequency_char<<" with frequency:"<<max_freq<<endl;
   }else
   {
    cout<<"No Duplicate found";
   }   
return 0;
}
