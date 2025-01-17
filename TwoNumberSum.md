Given an array of integers `nums` and an integer `target`, return _indices of the two numbers such that they add up to `target`_.

You may assume that each input would have **_exactly_ one solution**, and you may not use the _same_ element twice.

You can return the answer in any order.

**Example 1:**

**Input:** nums = [2,7,11,15], target = 9
**Output:** [0,1]
**Explanation:** Because nums[0] + nums[1] == 9, we return [0, 1].

**Example 2:**

**Input:** nums = [3,2,4], target = 6
**Output:** [1,2]

**Example 3:**

**Input:** nums = [3,3], target = 6
**Output:** [0,1]

#### Solution

Idea ?
Iterate over each element (first number), find the second number by (target - first number). Use a dictionary to store all previously visited elements and check whether the second number is already visited previously or not.

#### Algorithm

```
1. Start
2. Create a HashMap
3. Loop i = 0...N-1:
4. Define firstNumber = array[i]
5. Define secondNumber = (target - firstNumber)
6. If secondNumber present in HashMap, then
7. Return, found answer
8. Store the firstNumber and corrosponding index in HashMap
9. Stop
```

#### Complexity analysis

Since, we are storing each visiting element in dictionary and for worst case we would store all elements, hence the space complexity will be O(N)

We are iterating each and every element one by one, hence time complexity will be O(N)

------

What if, the problem was slightly modified!
Instead of returning indices, return the numbers.

Since we need to return the numbers, we can rearrange the elements because order does not matter now.

Idea ?
Sort the array in ascending order. Take two pointers, one pointing to first and another pointing to last element. Fist their some, if some is more than target then move large pointer to left side and vice versa. Keep doing that util first pointer crosses second or found the answer.

#### Algorithm

```
1. Start
2. Sort the array in ascending order
3. Define smallPointer = 0
4. Define largePointer = N-1
5. while smallPointer < largePointer:
6. Defind currentSum = array[smallPointer] + array[largePointer]
7. If currentSum == target, then return found answer
8. If currentSum < target, then increment smallPointer
9. If currentSum > target, then decrement largePointer
10. Stop
```

#### Complexity analysis

O(1) space, since we are not using any auxiliary space.
O(N*logN) time, for sorting the array.