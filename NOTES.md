# LeetCode: Two Sum

- slug: `two-sum`
- id: 1
- difficulty: Easy
- tags: Array, Hash Table
- url: https://leetcode.com/problems/two-sum/
- status: **solved_verified**
- detail: Local verified 3/3
- source: LeetCode public GraphQL (no login)
- learned_at: 2026-10-27T08:46:41.879354+00:00

## Problem
You are given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

 

Example 1:

Input: nums = [2,7,11,15], target = 9

Output: [0,1]

Explanation:

The sum of nums[0] and nums[1] is 2 + 7 = 9, which equals the target. Therefore, the indices [0, 1] are returned.

Example 2:

Input: nums = [3,2,4], target = 6

Output: [1,2]

Explanation:

The sum of nums[1] and nums[2] is 2 + 4 = 6, which equals the target. Therefore, the indices [1, 2] are returned.

Example 3:

Input: nums = [3,3], target = 6

Output: [0,1]

Explanation:

The sum of nums[0] and nums[1] is 3 + 3 = 6, which equals the target. Therefore, the indices [0, 1] are returned.

 

Constraints:

	- 2 4
	- -109 9
	- -109 9
	- Only one valid answer exists.

 

Follow-up: Can you come up with an algorithm that is less than O(n2) time complexity?

## Example testcases (from LeetCode)
```
[2,7,11,15]
9
[3,2,4]
6
[3,3]
6
```

## Solution (local)
```python
def two_sum(nums, target):
    seen = {}
    for i, x in enumerate(nums):
        need = target - x
        if need in seen:
            return [seen[need], i]
        seen[x] = i
    return []

```
