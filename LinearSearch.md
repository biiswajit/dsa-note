Idea ? 
We start searching from an index, and then we keep going towards one direction until we find the element or reach at the end.

#### Algorithm

```text
1. Start
2. Iterate the array from index number 0
3. If current element matched with the key return the current index
4. Increment the current index by 1
5. Repeat from step number 3 until reach at the end
6. Return -1 indicating key not found
7. Stop
```

#### Complexity analysis - Time complexity

In *Best case* we can find the key index first index, complexity O(1)
In *Worst case* key not present in the array, hence iterate over the entire array, complexity O(N)