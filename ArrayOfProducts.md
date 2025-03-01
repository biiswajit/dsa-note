#### Problem statement

Given an non-empty array of integers of length `n`. Return an array same length as input array containing products of all other elements from input array except self.

#### Idea ?

product[i] = (product of all elements from 0..i-1) * (product of all elements from i+1..n-1)

#### Algorithms

```text
1. start
2. calculate the product of all left elements and store them in an array
3. calculate the product of all right elements and store then in an array
4. final product will be the left products * right products
5. return the final products
6. stop
```

#### Complexity

O(3*N) time since we're iterating the array three times
O(3*N) space since we're creating three arrays of length n