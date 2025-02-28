
#### Problem description

Given an array of integers, find out the length of the longest peak.

An element can be called as peak if two adjacent elements are strictly less than the current element. `A[i-1] < A[i] > A[i+1]`. First and last element can be considered as peak.

Array can have multiple peaks find the the one with longest length and return the length of the longest peak.

#### Idea ?

Find the tip of the peak and expand from both side of the peak.

#### Algorithm

```text
1. Start
2. Start iteration from second index all the way to second last index, since first and last element can be considered as peaks
3. If current element is not the tip of peak, then continue
4. If current element is the tip of peak, then
	1. Expand left side of the peak
	2. Expand right side of the peak
	3. Calculate the distance you expanded, compare with the previously found peaks
5. Update the current pointer with the right edge of the peak and continue
6. Return the longest leangth found
7. Stop
```

#### Complexity analysis

To iterate over the array to find the tip of peaks and to expand the peak will take about O(N) time, where N is the number of elements in given array.

We're not using any auxiliary grow-able space, hence space complexity will be O(1).
