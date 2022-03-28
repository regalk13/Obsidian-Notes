## Peak Finding & Binary Search
> Resources (PDF):  [[Peak-Finding.pdf]]		

Given one-dimension array. Find a peak element in it. An array element is a peak if it is **NOT** smaller than its neighbors. For corner elements, we need to consider only one neighbor.

### Example:
```
Input: array[]= {5, 10, 20, 15}
Output: 20
The element 20 has neighbours 10 and 15,
both of them are less than 20.

Input: array[] = {10, 20, 15, 2, 23, 90, 67}
Output: 20 or 90
The element 20 has neighbours 10 and 15, 
both of them are less than 20, similarly 90 has neighbours 23 and 67.
```

#### Solutions
**Navie Approach:** The Array can be traversed and the element whose neighbours are less than that element can be returned.

> Code Resource: [[peak-find-naive.py.md]]

**Algorithm:**
1. If in the array, the first element is greater than the second or the last element is greater than the second last, print the respective element and terminate the program.
2. Else traverse the array from the second index to the second last index
3. If for an element array[i], it is greater than both its neighbours, i.e., array[i] > array[i-1] and array[i] > array[i+1], then print that element and terminate.

![[Peak-find-naive.png]]


**Efficient Solution:** 
Divide and conquer can be used to find a peak in O(log n) time. The idea is based on the technique of [[Binary Search]] to check if the middle element is the peak element or not. If the middle element is not the peak element, then check if the element on the right side is greater than the middle element then there is always a peak element on the right side. If the element on the left side is greater than the middle element then there is always a peak element on the left side. Form a recursion and the peak element can be found in log n time. 

> Code Resource: [[peak-find-efficent.py.md]]

**Algorithm:**

1. Create two variables, l and r, initialize l = 0 and r = n-1
2. Iterate the steps below till l <= r, lowerbound is less than the upperbound
3. Check if the mid value or index mid = (l+r)/2, is the peak element or not, if yes then print the element and terminate.
4. Else if the element on the left side of the middle element is greater then check for peak element on the left side, i.e. update r = mid – 1
5. Else if the element on the right side of the middle element is greater then check for peak element on the right side, i.e. update l = mid + 1

![[peak-find-better-solution.png]]

#### Aditional Sources:
- [YouTube video](https://youtu.be/NFvAD5na5oU)
- [MIT Class](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/lecture-videos/lecture-1-algorithmic-thinking-peak-finding/)