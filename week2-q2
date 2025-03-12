#include<iostream>
#include<vector>
using namespace std;

void findTriplets(vector<int>& arr, int n) {
    bool found = false;

    // Iterate over k (the sum)
    for(int k = 2; k < n; k++) {
        int i = 0, j = k - 1;

        // Two-pointer approach to find arr[i] + arr[j] == arr[k]
        while(i < j) {
            if(arr[i] + arr[j] == arr[k]) {
                cout << "Indices: " << i << ", " << j << ", " << k << endl;
                found = true;
                i++; j--; // Move both pointers to find other possible pairs
            } else if(arr[i] + arr[j] < arr[k]) {
                i++; // Increase sum
            } else {
                j--; // Decrease sum
            }
        }
    }

    if(!found) {
        cout << "No triplet found." << endl;
    }
}

int main() {
    int n;
    cout << "Enter the size of the array: ";
    cin >> n;

    vector<int> arr(n);
    cout << "Enter the elements of the sorted array: ";
    for(int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    findTriplets(arr, n);
    return 0;
}
