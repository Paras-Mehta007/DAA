#include<iostream>
#include<vector>
using namespace std;

int comparison = 0;
int inversion=0;

void merge(vector<int>& arr, int st, int end, int mid)
{
    int n1 = mid - st + 1;
    int n2 = end - mid;
    
    vector<int> L(n1), R(n2);
    
    for (int i = 0; i < n1; i++)
    {
        L[i] = arr[st + i];
    }
    for (int j = 0; j < n2; j++)
    {
        R[j] = arr[mid + 1 + j];
    }
    
    int i = 0, j = 0;
    int k = st;
    
    while (i < n1 && j < n2)
    {
        comparison++;
        if (L[i] <= R[j])
        {
            arr[k] = L[i];
            i++;
        }
        else
        {
            arr[k] = R[j];
            inversion=(mid-st+1);
            j++;
        }
        k++;
    }
    
    while (i < n1)
    {
  
        arr[k] = L[i];
        i++;
        k++;
    }
    
    while (j < n2)
    {
       
        arr[k] = R[j];
        j++;
        k++;
    }
}

void mergesort(vector<int>& arr, int start, int end)
{
    if (start >= end)
    {
        return;
    }
    
    int mid = start + (end - start) / 2;
    
    mergesort(arr, start, mid);
    mergesort(arr, mid + 1, end);
    
    merge(arr, start, end, mid);
}

void printvector(const vector<int>& arr)
{
    for (int i = 0; i < arr.size(); i++)
    {
        cout << arr[i] << " ";
    }
    cout << endl;
}

int main()
{
    int n;
    cout << "Enter the size of the array: ";
    cin >> n;
    
    vector<int> arr(n);
    
    cout << "Enter the elements of the array: ";
    for (int i = 0; i < n; i++)
    {
        cin >> arr[i];
    }
    
    cout << "Before sorting: ";
    printvector(arr);
    
    mergesort(arr, 0, n - 1);
    
    cout << "After sorting: ";
    printvector(arr);
    
    cout << "Number of comparisons: " << comparison << endl;
    
    cout << "Number of inversion: " << inversion << endl;
    
    return 0;
}
