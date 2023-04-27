# Linear Search in C

Linear search is a simple search algorithm that searches for an element in an array by sequentially checking each element until a match is found. It has a time complexity of O(n), where n is the number of elements in the array.

This repository contains an implementation of linear search in C with the following function:

linear_search: searches for an element in an array and returns its index if found, or -1 if not found.

## Output

```
Enter the size of the array: 5
Enter 5 integers: 2 4 6 8 10
Enter the element to search: 6
Element found at index 2
```

In this output, we first prompt the user to enter the size of the array and its elements. We then prompt the user to enter the element to search for, which is 6 in this case. The linear_search function searches for the element in the array and returns its index (2). If the element is not found in the array, the function returns -1.

## Getting Started

To use the linear search implementation, follow these steps:

Download or clone the repository.
Include the linear_search.h header file in your program.
Declare an array and its size.
Call the linear_search function and pass the array, its size, and the element to search for.
Check the return value of the function to determine if the element was found or not.

```
#include <stdio.h>
#include "linear_search.h"

#define MAX_SIZE 100

int main() {
    int arr[MAX_SIZE], size, search, index;

    printf("Enter the size of the array: ");
    scanf("%d", &size);

    printf("Enter %d integers: ", size);
    for (int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Enter the element to search: ");
    scanf("%d", &search);

    index = linear_search(arr, size, search);
    if (index == -1) {
        printf("Element not found\n");
    } else {
        printf("Element found at index %d\n", index);
    }

    return 0;
}
```

