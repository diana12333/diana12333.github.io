---
title: "Leetcode: Two Sums"
date: 2020-12-31
categories:
  - Post
---


## Two pass hash table

Can make use of the 
```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        l = {}
        for enum,num in enumerate(nums):
            l[num] = enum
        for enum,num in enumerate(nums):
            comp = target - num
            if comp in l.keys():
                if not l.get(comp,-1)==enum:
                    return [l[comp],enum]
```