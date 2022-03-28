```python
def partition(start, end, array):

    # Pivot
    pivot_index = start
    pivot = array[pivot_index]
    print(f"pivot index: {pivot_index}")
    print(f"pivot: {pivot}")

    # This loop runs till start pointer crosses
    # end pointer, and when it does we swap the
    # pivot with element on end pointer
    while start < end:
        while start < len(array) and array[start] <= pivot:
            start += 1
            print(f"New Start: {start}")

        while array[end] > pivot:
            end -= 1
            print(f"To End: {end}")

        if (start < end):
            print(f"Swap in progress: {array[start]} - {array[end]} to:")
            array[start], array[end] = array[end], array[start]
            print(f"{array[start]} - {array[end]}")

    array[end], array[pivot_index] = array[pivot_index], array[end]
    print(f"Next pivot {end}")

    return end

def quick_sort(start, end, array):

    if (start < end):

        p = partition(start, end, array)

        quick_sort(start, p-1, array)
        quick_sort(p+1, end, array)



array = [10, 7, 8, 9, 1, 5]
quick_sort(0, len(array) - 1, array)

print(f'Sorted array: {array}')
```
**Output**
``Sorted array: 1 5 7 8 9 10``

**Complexity**

We have a average case of 0(n lg n) and a worst case of 0(n²).
