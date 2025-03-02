// Find first and last Occurrence
#include<iostream>
using namespace std;

int binaryduplicate(int arr[], int n, int key) {
    int first = -1, last = -1;
    int start = 0, end = n - 1;

    // Find the first occurrence of key
    while (start <= end) {
        int mid = start + (end - start) / 2;
        if (arr[mid] == key) {
            first = mid;
            end = mid - 1;  // Move left to find the first occurrence
        } else if (arr[mid] < key) {
            start = mid + 1;
        } else {
            end = mid - 1;
        }
    }

    if (first == -1) return 0;  // Key not found

    start = 0, end = n - 1;

    // Find the last occurrence of key
    while (start <= end) {
        int mid = start + (end - start) / 2;
        if (arr[mid] == key) {
            last = mid;
            start = mid + 1;  // Move right to find the last occurrence
        } else if (arr[mid] < key) {
            start = mid + 1;
        } else {
            end = mid - 1;
        }
    }

    return last - first + 1;
}

int main() {
    int arr[13] = {1, 2, 3, 4, 5, 5, 5, 5, 6, 6, 6, 7, 8};
    int n = 13;
    int key;
    cout << "Enter the key between 1 to 8: ";
    cin >> key;

    int count = binaryduplicate(arr, n, key);
    cout << "Number of duplicates: " << count << endl;

    return 0;
}
