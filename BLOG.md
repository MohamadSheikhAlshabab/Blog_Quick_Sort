# Quick Sort

- Like Merge Sort, Quick Sort is a Divide and Conquer algorithm.
- It picks an element as a pivot and partitions the given array around the picked pivot.
- There are many different versions of quickSort that pick pivot in different ways.

## Quick sort Description

- Quick sort is a highly efficient sorting algorithm and is based on the partitioning of an array of data into smaller arrays.
- A large array is partitioned into two arrays one of which holds values smaller than the specified value.
- say pivot, based on which the partition is made and another array holds values greater than the pivot value.
- Quick sort partitions an array and then calls itself recursively twice to sort the two resulting subarrays.
- This algorithm is quite efficient for large-sized data sets as its average and worst-case complexity are O(n Logn) and  O(n^2). respectively.
- ![img](https://www.tutorialspoint.com/data_structures_algorithms/images/quick_sort_partition_animation.gif)
- ![img](https://www.geeksforgeeks.org/wp-content/uploads/gq/2014/01/QuickSort2.png)

## Approach & Efficiency

### Worst Case

- __Time Complexity__: O(n^2)
- __Space Complexity__: O(log(n))
  
  - ALGORITHM Partition:
    - Step 1 − Choose the highest index value has a pivot
    - Step 2 − Take two variables to point left and right of the list excluding pivot
    - Step 3 − left points to the low index
    - Step 4 − right points to the high
    - Step 5 − while the value at left is less than pivot move right
    - Step 6 − while the value at the right is greater than the pivot move left
    - Step 7 − if both step 5 and step 6 does not match swap left and right
    - Step 8 − if the left value is greater or equal the right value, the point where they met is the new pivot
  
- ALGORITHM QuickSort:
  - Step 1 − Make the right-most index value pivot
  - Step 2 − partition the array using pivot value
  - Step 3 − quicksort left partition recursively
  - Step 4 − quicksort right partition recursively

### Pseudo Code

          ALGORITHM QuickSort(arr, left, right)
              if left < right
                  // Partition the array by setting the position of the pivot value 
                  DEFINE position <-- Partition(arr, left, right)
                  // Sort the left
                  QuickSort(arr, left, position - 1)
                  // Sort the right
                  QuickSort(arr, position + 1, right)

          ALGORITHM Partition(arr, left, right)
              // set a pivot value as a point of reference
              DEFINE pivot <-- arr[right]
              // create a variable to track the largest index of numbers lower than the defined pivot
              DEFINE low <-- left - 1
              for i <- left to right do
                  if arr[i] <= pivot
                      low++
                      Swap(arr, i, low)

               // place the value of the pivot location in the middle.
               // all numbers smaller than the pivot are on the left, larger on the right. 
               Swap(arr, right, low + 1)
              // return the pivot index point
               return low + 1

          ALGORITHM Swap(arr, i, low)
              DEFINE temp;
              temp <-- arr[i]
              arr[i] <-- arr[low]
              arr[low] <-- temp

## Solution

[url](https://drive.google.com/file/d/1qTp-FVEq7w3xYMA0lKIjFuyyTZ91ruHY/view?usp=sharing)
