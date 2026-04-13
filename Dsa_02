#include <stdio.h>

int binarySearch(int arr[], int key, int low, int high) {
    while (low <= high) {
        int mid = low + (high - low) / 2;

        if (arr[mid] == key)
            
            return mid; 
        else if (arr[mid] < key)
            low = mid + 1;
        else
            high = mid - 1;
    }
  
    return low;
}


void binaryInsertionSort(int arr[], int n) {
    int i, j, position, key;

    for (i = 1; i < n; i++) {
        key = arr[i]; 
        j = i - 1;

        
        position = binarySearch(arr, key, 0, j);

        while (j >= position) {
            arr[j + 1] = arr[j];
            j--;
        }

        
        arr[j + 1] = key;
    }
}


void printArray(int arr[], int n) {
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    int array[] = {9, 7, 2, 6, 4};
    int size = sizeof(array) / sizeof(array[0]);

    printf("Original array: ");
    printArray(array, size);

    binaryInsertionSort(array, size);

    printf("Sorted array: ");
    printArray(array, size);

    return 0;
}
