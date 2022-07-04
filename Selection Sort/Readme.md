The selection sort algorithm sorts an array by repeatedly finding the minimum element (considering ascending order) from unsorted part and putting it at the beginning. The algorithm maintains two subarrays in a given array.

The subarray which is already sorted. 
Remaining subarray which is unsorted.

In every iteration of selection sort, the minimum element (considering ascending order) from the unsorted subarray is picked and moved to the sorted subarray. 

**Approach:**

Initialize minimum value(min_idx) to location 0

Traverse the array to find the minimum element in the array

While traversing if any element smaller than min_idx is found then swap both the values.

Then, increment min_idx to point to next element

Repeat until array is sorted

Complexity Analysis of Selection Sort:
Time Complexity: The time complexity of Selection Sort is O(N2) as there are two nested loops.

Auxiliary Space: O(1) as the only extra memory used is for temporary variable while swapping two values in Array.
