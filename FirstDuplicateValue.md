#### Problem statement

Given an integer array, where each element of array in between [1..n], where n is the number of elements in input array.

Find the first duplicate value present in the array (reading from left to right).

#### Idea ?

Cyclic sort! 
`i` is the current index
`arr[i]` is the current element
then `arr[i]` element suppose to present in `arr[i] - 1` index if the array was sorted.

#### Algorithm

```text
1. start
2. iterate from left to right
3. find the actual index of the current element (current element - 1)
4. if actual index is already marked then current element is the first duplicate
5. if actual index is not marked then mark the actual index
6. return -1 indicating there are no duplicate elements present
7. stop
```

#### Complexity analysis

O(N) time since we are iterating the array from left to right once

O(1) space since we are not using any extra space to mark elements (we're negate the elements in actual index)