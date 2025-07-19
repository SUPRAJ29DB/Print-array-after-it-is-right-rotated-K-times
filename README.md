# Print-array-after-it-is-right-rotated-K-times
To right rotate an array K times means shifting each element to the right K positions — the elements at the end come back to the beginning. 
```
#include <stdio.h>

int main() {
    int n, k, i;

    // Input size and elements
    printf("Enter size of array: ");
    scanf("%d", &n);

    int arr[n];
    printf("Enter array elements:\n");
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Input number of rotations
    printf("Enter number of right rotations: ");
    scanf("%d", &k);

    // Normalize rotations if k > n
    k = k % n;

    // Create a temporary array
    int rotated[n];

    // Place elements at new positions
    for (i = 0; i < n; i++) {
        rotated[(i + k) % n] = arr[i];
    }

    // Print rotated array
    printf("Array after %d right rotations:\n", k);
    for (i = 0; i < n; i++) {
        printf("%d\t", rotated[i]);
    }
    printf("\n");

    return 0;
}
```

//
// Created by Suprakash Ghosh on 19-07-2025.
//
