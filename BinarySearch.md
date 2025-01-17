Note: Binary Search only applicable for an array which is sorted in ascending or descending order.

Idea ?
Divide the problem in half and eliminate one half and explore another half.

#### Algorithm

```text
1. Start
2. Initialize startIdx = 0, endIdx = N
3. While startIdx <= endIdx, then
4. Initialize mid = ((endIdx - startIdx) / 2) + startIdx
5. If e[mid] == key, then key found return
6. Else if e[mid] < key, then startIdx = mid + 1
7. Else if e[mid] > key, then endIdx = mid - 1
8. Repeat from step 3
9. Key not found return -1
10. Stop
```

#### Complexity analysis - Time complexity

Best Case: Key is the first middle element, complexity O(1)

Worst Case: 

```
0st level ---> problem size N   => N/2^0
1st level ---> problem size N/2 => N/2^1
2nd level ---> problem size N/4 => N/2^2
.
.
.
kth level ---> problem size N/2^k = 1

N = 2^k, where k is the number of iterations we are performing to get a problem size 1

log2(N) = log2(2^k)
log2(N) = klog2(2)
k = log2(N) / log2(2)
k = log2(N) / 1
k = log2(N)
```

In worst case the binary search will take O(log(N)) complexity