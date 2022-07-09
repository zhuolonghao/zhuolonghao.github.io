  ---
layout: post
title: "[Coding] Data Structure: List and String"
---

{{ page.title }}
================

<p class="meta">Dec 2022 - Charlotte, NC</p>

This post is my personal note from practicing leetcodes as suggested by [Grind75](https://www.techinterviewhandbook.org/grind75?topics=array&weeks=3&hours=6#) and its [handbook](https://www.techinterviewhandbook.org/algorithms/array/).

# By Topic

# By Techniques

### Backtracking
This is a general algorithm for finding all (or some) solutions to some computational problems: it incrementally builds candidates to the solutions, and abandons a candidate as soon as it determines that this candidate cannot lead to a final solution.

[39. Combination Sum](https://leetcode.com/problems/combination-sum/): find a list of all unique combinations of candidates where the chosen numbers sum to target. For variations, see [target=fixed-length](https://leetcode.com/problems/combinations/), [candidate can only be used *once*](https://leetcode.com/problems/combination-sum-ii/), and [used-once](https://leetcode.com/problems/combination-sum-iii/).
```python
class Solution:
    def combinationSum(self, candidates: List[int], target: int) -> List[List[int]]:

        def backtrack(remain, comb, start):
            # exit condition (pertaining to target)
            if remain == 0:
                results.append(list(comb))
                return
            elif remain < 0:
                return
            # search over feasible set for combination
            for i in range(start, len(candidates)):
                # act first, backtrack later
                comb.append(candidates[i])
                # start=i, for unlimited use of values.
                # start=i+1, for one-time use of values.
                backtrack(remain - candidates[i], comb, i)
                # backtrack
                comb.pop()

        results = []
        backtrack(target, [], 0)
        return results
```

### Divide and conquer
This is one of the most powerful algorithm, with a simple idea: find a solution for the base case, and work up to a full problem in a recursive manner.

[169. Majority Element](https://leetcode.com/problems/majority-element/): Given an array nums of size n, return the majority element.
```python
class Solution:       
    def majorityElement(self, nums, lo=0, hi=None):
        def majority_element_rec(lo, hi):
            # base case-1: there's one element in nums
            if lo == hi:
                return nums[lo]

            # Divider: starts
            mid = (hi+lo)//2
            left = majority_element_rec(lo, mid)
            right = majority_element_rec(mid+1, hi)
            # Divider: ends

            # Base case-2: there're two elements in nums, and they are same
            if left == right:
                return left
            # Base case-3: there're three elements in nums
            left_count = sum(1 for i in range(lo, hi+1) if nums[i] == left)
            right_count = sum(1 for i in range(lo, hi+1) if nums[i] == right)
            return left if left_count > right_count else right

        return majority_element_rec(0, len(nums)-1)
```

### Greedy
This algorithm is often case-by-case, and rely heavily on how one approach the question.

[57. Insert Interval](https://leetcode.com/problems/insert-interval/): Insert newInterval into intervals such that intervals is still sorted in ascending order by starti and intervals still does not have any overlapping intervals


# Key Functions
### List

| Operation             | Function                 |
|-------------------------|-----------------------------|
| sort a list           | xxx.sort()                  |
| sort a list  | yyy = sorted(xxx)                    |        
| sort a list by a second list |  [x for _, x in sorted(zip(yyy, xxx))] |
| sort a list of lists by 1st element   | xxx.sort(key=lambda x:x[0])|
| sort a list of lists by 1st element   | yyy = sorted(xxx, key=lambda x: x[0])|
| sort a list of lists by length| xxx.sort(key=len)
|
|search a value in a list| xxx.index(value) |
|search if a value in a list | xxx in value |
|search a value in a sorted list | bisect_left(xxx, value) |
|
| insert a value    | xxx.insert(index, value)  
| insert a list    | xxx.extend(yyy)        
| insert a value at the end  | xxx.append(value)        |
| insert a value in a sorted list | xxx.insort_left(value) |
|
| remove a value | xxx.remove(value) |
| remove a value by index | xxx.pop(index) |
| remove a value by index | del xxx[index]   |

### dictionary
| Operation | Function |
|---|---|
|sort by value | sorted(_dict.items, key = lambda x: x[1]) |
| return key with max value | max(_dict.keys(), key=_dict.get) |


### Set
| Description             | Function-1        | Function-2               |
|-------------------------|-------------------|--------------------------|
| create a new set        | _set = set()  | |
| add an item | _set.add(value)| |
| set: s belongs to t | s.issubset(t)     | s <= t |
| set: union | s.union(t)  | s \| t   |                   
| set: intersection  | s.intersection(t) | s & t                    |                  
| set: x in s but not in t| s.diference(t)    | s - t                    |                  

### String
| Description                        | Function-1                        | Example |
|------------------------------------|-----------------------------------|---------|
| return left-most index of "chars" in string "s" | s.find("chars"), scanning from left to right| s = "01234567890"; s.find("012") = 0; s.find("0") = 0  |
| return right-most index of "chars" in string "s" | s.rfind("chars"), scanning from left to right| s = "01234567890"; s.rfind("012") = 0; s.rfind("0") = 10 |
| split a string, "s", to a list of letters| s.split() | s = "ab c ab"; s.split() = ['ab', 'c', 'ab'] |                       
| join a list of *strings*, "s_list" to one string      |  "".join(s_list) | s = "".join(['ab', 'c', 'ab']); s = "abcab" |                                       
| reverse a string  | reversed = s[::-1]| s = "abcab", reversed = "bacba" |

### Matrix: Traverse  

| 1 | 2 | 3 | 4 |
|---|---|---|---|
| 5 | 6 | 7 | 8 |
| 9 | 10| 11| 12|
|13 | 14| 15| 16|   

- Scan by row (column):
  - row scan: ```[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16]```
  - column scan: ```[1, 5, 9, 13, 2, 6, 10, 14, 3, 7, 11, 15, 4, 8, 12, 16]```
```python
# Below is row scan.
for row in range(4):
      for col in range(4):
        ans.append(dp[row][col])
# column scan: switch row and col in for-loops
```

- Scan triangular matrix  
  - lower: ```[1, 5, 6, 9, 10, 11, 13, 14, 15, 16]```
  - upper: ```[1, 2, 6, 3, 7, 11, 4, 8, 12, 16]```
  ``` python
  # Below is to get lower triangular matrix
  for row in range(4):
      for col in range(row+1):
        ans.append(dp[row][col])
  # Upper triangular matrix: switch row and col in for-loops
  ```
  - lower: ```[1, 5, 9, 13, 6, 10, 14, 11, 15, 16]```
  - upper: ```[1, 2, 3, 4, 6, 7, 8, 11, 12, 16]```
  ```python
  for col in range(4):
      for row in range(col,4):
        ans.append(dp[row][col])
  ```

- Scan along diagonal
  - Bottom-left to Top-right: ```[1, 5, 2, 9, 6, 3, 13, 10, 7, 4, 14, 11, 8, 15, 12]```
  - Top-right to Bottom-left: ```[1, 2, 5, 3, 6, 9, 4, 7, 10, 13, 8, 11, 14, 12, 15]```
  ```python
# Below is to scan from bottom-left to top-right
ans = [[] for _ in range(nrow+ncol-1)]
for row in range(nrow):
      for col in range(ncol):
        ans[row+col].append(arr[row][col])
ans2 = []
for i in ans: ans2.extend(i)
# top-right to bottom left: switching if conditions
  ```
  - Upper triangular: ```[1, 6, 11, 16, 2, 7, 12, 3, 8, 4]```
  - Lower triangular: ```[1, 6, 11, 16, 5, 10, 15, 9, 14, 13]```
  ```python
  for gap in range(4):
      row = 0
      col = row + gap
      while (row >=0) & (row < 4) & (col >= 0) & (col < 4):
         ans.append(dp[row][col])
         row += 1
         col += 1
  ```
  - Left-upper triangular: ```[1, 5, 2, 9, 6, 3, 13, 10, 7, 4]```
  ```python
  ans = []
  for _sum in range(4):
      for col in range(_sum+1):  
        row  = _sum - col
        ans.append(dp[row][col])
  ```


### Difference btw "and" and "&"
In most cases, they're equivalent.

Sometimes, "and" is preferred to "&" because "and" is a *lazy evaluation*, meaning if the first statement is False, it does not check the second statement and returns False immediately, while "&" would evaluate all statements.  

### Difference btw "self." and "clf."
Here is a reference from [stackoverflow](https://stackoverflow.com/questions/7554738/python-self-no-self-and-cls)
```python
class Foo(object):

    # you couldn't use self. or cls. out here, they wouldn't mean anything

    # this is a class attribute
    thing = 'athing'

    def __init__(self, bar):
        # I want other methods called on this instance of Foo
        # to have access to bar, so I create an attribute of self
        # pointing to it
        self.bar = bar

    @staticmethod
    def default_foo():
        # static methods are often used as alternate constructors,
        # since they don't need access to any part of the class
        # if the method doesn't have anything at all to do with the class
        # just use a module level function
        return Foo('baz')

    @classmethod
    def two_things(cls):
        # can access class attributes, like thing
        # but not instance attributes, like bar
        print cls.thing, cls.thing
```



### Package: colletions

| Functions                          | Outcome or Description                                                         |
|------------------------------------|--------------------------------------------------------------------------------|
| _dict = collections.Counter(nums)  | collections.Counter("Hello") = Counter({'l': 2, 'H': 1, 'e': 1, 'o': 1})       |
| _dict = collections.defaultdict(int) | create a dictionary whose values are integer |
| _dict = collections.defaultdict(list) | create a dictionary whose values are list   |
