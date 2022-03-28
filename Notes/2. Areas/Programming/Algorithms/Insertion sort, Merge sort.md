Why? [[Sorting]]
## Insertion Sort
> Resource (PDF) [[Insert-Sort.pdf]]

Insertion-Sort (A, n) -> A[1 .. n]
    for j <- 2 to n
	 insert key A[j] into the (already sorted) sub-array A[1 .. j-1].
	 by pairwise key-swaps down to its right position.

![[Insert-Sort.png]]


**Example of Execution:**
![insertion-sort](https://media.geeksforgeeks.org/wp-content/uploads/insertionsort.png)

**Another Example:**
**12**, 11, 13, 5, 6
Let us loop for i = 1 (second element of the array) to 4 (last element of the array)
i = 1. Since 11 is smaller than 12, move 12 and insert 11 before 12 
**11,  12**, 13, 5, 6
i = 2. 13 will remain at its position as all elements in A[0..I-1] are smaller than 13 
**11, 12, 13**, 5, 6
i = 3. 5 will move to the beginning and all other elements from 11 to 13 will move one position ahead of their current position. 
**5, 11, 12, 13**, 6
i = 4. 6 will move to position after 5, and elements from 11 to 13 will move one position ahead of their current position. 
**5, 6, 11, 12, 13**

**Code Example:**
Simple insert sort python code: [[insert-sort.py]]

If you see the before code, its 0(n²) time, really inefficient, so we can optimize the algorithm whit [[Binary Search]].

## Merge Sort

Like [[QuickSort]], Merge Sort is a [[Divide and Conquer]] algorithm. It divides the input array into two halves, calls itself for the two halves, and then merges the two sorted halves. **The merge() function** is used for merging two halves. The merge(arr, l, m, r) is a key process that assumes that arr[l..m] and arr[m+1..r] are sorted and merges the two sorted sub-arrays into one. See the following C implementation for details.

```
MergeSort(arr[], l,  r)
If r > l
     1. Find the middle point to divide the array into two halves:  
             middle m = l+ (r-l)/2
     2. Call mergeSort for first half:   
             Call mergeSort(arr, l, m)
     3. Call mergeSort for second half:
             Call mergeSort(arr, m+1, r)
     4. Merge the two halves sorted in step 2 and 3:
             Call merge(arr, l, m, r)
```

**See the following diagram:**
![Merge-Sort-Tutorial](https://media.geeksforgeeks.org/wp-content/cdn-uploads/Merge-Sort-Tutorial.png)

**Code Example:**[[merge-sort.py]]

**Additional Resource:**
- [YouTube Video](https://youtu.be/JSceec-wEyw)
- [MIT Class](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/lecture-videos/lecture-3-insertion-sort-merge-sort/)