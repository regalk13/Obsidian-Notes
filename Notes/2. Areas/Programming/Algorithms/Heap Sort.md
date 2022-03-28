## Heaps & Heap Sort

### Priority Queue
A data structure implementing a set S of elements, each associated with a key, supporting the following operations:

**insert(S, x):** insert element $x$ into set $S$
**max(S):** return element of $S$ with largest key
**extract_max(S):** return element of $S$ with largest key and remove it from $S$
**increase_key(S, x, k):** increase the value of element $x$' s key to new value $k$
(assumed to be as large as current value)

### Heap 
- Implementation of a priority queue
- An array, visualized as a nearly complete binary tree
- Max Heap Property: The key of a node is >= than the keys of its children (Min Heap defined analogously)

![[heap.png]]
### Heap as a Tree
- **root of tree:** first element in the array, corresponding to $i = 1$
- **parent(i) = i/2:** returns index of node's parent
- **left(i) = 2i:** returns index of node's left child
- **right(i) = 2i+1:** returns index of node's right child

### Heap Operations

**build_max_heap:** produce a max-heap from an unordered array

**max_heapify:** correct a _single_ violation of the heap property in a subtree at its root

**insert, extract_max, heapsort**

## More content
Read more about this in the PDF: [[Heap-Sort.pdf]]



