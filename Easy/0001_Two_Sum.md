# 1. Two Sum

## Problem Statement

Given an array of integers `nums` and an integer `target`, return the indices of the two numbers such that they add up to the target.

You may assume that each input has exactly one solution.

---

## Intuition

Check every possible pair of numbers.

If their sum equals the target, return their indices.

---

## Logic Explanation (Tanglish)

Namma array-la irukkura ovvoru number-um ella remaining numbers kooda compare panrom.

Example:

```python
nums = [2,7,11,15]
target = 9
```

First:

```python
2 + 7 = 9
```

Target match aagiduchu.

So indices:

```python
[0,1]
```

Return panniduvom.

---

## Python Code (Brute Force)

```python
class Solution:
    def twoSum(self, nums, target):

        for i in range(len(nums)):

            for j in range(i + 1, len(nums)):

                if nums[i] + nums[j] == target:

                    return [i, j]
```

---

## Dry Run

### Input

```python
nums = [2,7,11,15]
target = 9
```

### Iteration 1

```python
i = 0
j = 1
```

Check:

```python
nums[0] + nums[1]

2 + 7 = 9
```

Condition:

```python
9 == 9
```

True

Return:

```python
[0,1]
```

---

## Line by Line Explanation (Tanglish)

```python
for i in range(len(nums)):
```

👉 Outer loop.

👉 Oru number-ah select panrom.

First iteration:

```python
i = 0
```

Value:

```python
nums[i] = 2
```

---

```python
for j in range(i + 1, len(nums)):
```

👉 Current number-ku next irukkura elements-ah check panrom.

```python
j = 1
```

Value:

```python
nums[j] = 7
```

---

```python
if nums[i] + nums[j] == target:
```

👉 Rendum add panrom.

```python
2 + 7 = 9
```

Target-oda compare panrom.

---

```python
return [i, j]
```

👉 Answer indices return panrom.

```python
[0,1]
```

---

## Time Complexity

```python
O(n²)
```

Reason:

Every element is compared with every other element.

---

## Space Complexity

```python
O(1)
```

No extra data structure used.

---

## Pattern Learned

- Arrays
- Nested Loops
- Brute Force Search

---

## Revision Notes

Whenever the problem asks:

- Find a pair
- Find two numbers
- Target sum

First think:

```python
Nested Loop (Brute Force)
```

Then optimize using:

```python
Hash Map
```
