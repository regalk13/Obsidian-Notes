### Code:
```python
# Find the peak element in the array
def findPeak(arr, n) :
 
    # first or last element is peak element
    if (n == 1) :
      return 0
    if (arr[0] >= arr[1]) :
        return 0
    if (arr[n - 1] >= arr[n - 2]) :
        return n - 1
  
    # check for every other element
    for i in range(1, n - 1) :
  
        # check if the neighbors are smaller
        if (arr[i] >= arr[i - 1] and arr[i] >= arr[i + 1]) :
            return i
             
# Driver code.
arr = [ 1, 3, 20, 4, 1, 0 ]
n = len(arr)
print("Index of a peak point is", findPeak(arr, n))
```
**Output:**
``Index of a peak point is 2

**Complexity**
-   **Time complexity:** O(n).   
    One traversal is needed so the time complexity is O(n)
-   **Space Complexity:** O(1).   
    No extra space is needed, so space complexity is constant