---
layout: post
title: "[Coding] Data Structure: List and String"
---

{{ page.title }}
================

<p class="meta">Dec 2022 - Charlotte, NC</p>

# By Topic

Let's recap what we looked at in this explore card:

- intro: accessing, capacity vs length
  - [485](https://leetcode.com/problems/max-consecutive-ones/): curr_ and max_
  - [977](https://leetcode.com/problems/squares-of-a-sorted-array/): result = [0] * n, left = 0, right = n - 1

- insert items into lists
  - [1089](https://leetcode.com/problems/duplicate-zeros/): use .pop and .insert
  - [88](https://leetcode.com/problems/merge-sorted-array/): p1 = 0, p2 = 0, for i in range(n+m):

- delete items from lists
  - [27](https://leetcode.com/problems/remove-duplicates-from-sorted-array/):

- search for items in an list
  - [1346](https://leetcode.com/problems/check-if-n-and-its-double-exist/):
  - [941](https://leetcode.com/problems/valid-mountain-array/): walk-up to the peak, and step down to the trough.

- in-place algorithms
  - [1299](https://leetcode.com/problems/replace-elements-with-greatest-element-on-right-side/):

# By Approach

- Approach: One Pass, time complexity = O(n)
  - [485](https://leetcode.com/problems/max-consecutive-ones/): curr_ and max_
  - [1089](https://leetcode.com/problems/duplicate-zeros/): use .pop and .insert
  - [1346](https://leetcode.com/problems/check-if-n-and-its-double-exist/):
  - [941](https://leetcode.com/problems/valid-mountain-array/): walk-up to the peak, and step down to the trough.
  - [217](https://leetcode.com/problems/contains-duplicate/): _dict={} for i in nums: if i not in _dict
  - [1](https://leetcode.com/problems/two-sum/): _dict={} for i in nums: resid = target - i if resid in _dict,

- Approach: Two Passes, time complexity = O(n)
  - [905](https://leetcode.com/problems/sort-array-by-parity/):  return ([x for x in A if x % 2 == 0] + [x for x in A if x % 2 == 1])

- Approach: Two Pointers, time complexity = O(n)
  - [977](https://leetcode.com/problems/squares-of-a-sorted-array/): left = 0, right = n - 1, for i in reversed(range(n))
    - it's superior to mine (where i started with searching for zero in the middle, and two pointers goes to different directions)
  - [88](https://leetcode.com/problems/merge-sorted-array/): p1 = 0, p2 = 0, for i in range(n+m):
  - [1299](https://leetcode.com/problems/replace-elements-with-greatest-element-on-right-side/): p1 = 0, p2 = 0, while p0 < n-1
  - [283](https://leetcode.com/problems/move-zeroes/): i=0, j=0, while i < len(nums)
  - [905](https://leetcode.com/problems/sort-array-by-parity/):  i=0, j=len(A)-1, while i < j:
  - [487](https://leetcode.com/problems/max-consecutive-ones-ii/): p1=0, p2=0, while p1 < len(nums)
  - [487](https://leetcode.com/problems/max-consecutive-ones-ii/): curr_run, prev_run  = 0, 0, maxRun = max(maxRun, prevOnes + 1 + currOnes)
  - [977](https://leetcode.com/problems/squares-of-a-sorted-array/): result = [0] * n, left = 0, right = n - 1, for i in reversed(range(n)):
  - [121](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/): min_price = 0, max_profit = 0

- Approach: Three-Pointers
  - [75](https://leetcode.com/problems/sort-colors/), p0 = curr = 0, p2 = len(nums)-1 while curr <= p2
- Approach: Sliding Window, time complexity = O(n)
  - [487](https://leetcode.com/problems/max-consecutive-ones-ii/):longest_sequence=0, left, right = 0, 0, num_zeroes=0, while right < len(nums):

- Approach: Set
  - [414](https://leetcode.com/problems/third-maximum-number/): set(nums), .remove(), .remove(), .remove()
  - [448](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/): set operation: set() - set()
  - [217](https://leetcode.com/problems/contains-duplicate/): len(set(nums)) == len(nums)

- Approach: Dynamic Programming
  - [53](https://leetcode.com/problems/maximum-subarray/): curSum = max(num, curSum + num) maxSum = max(maxSum, curSum)
  - [238](https://leetcode.com/problems/product-of-array-except-self/): for i in range(1,len(nums)):  answer[i] = answer[i] * tmp; for i in reversed(range(len(nums))): answer[i] = answer[i] * tmp;

- Approach: Binary search

  - [74](https://leetcode.com/problems/search-a-2d-matrix/): left, right = 0, m * n - 1 while left <= right: pivot_idx = (left + right) // 2  *pivot_element = matrix[pivot_idx // n][pivot_idx % n]*
  - [240](https://leetcode.com/problems/search-a-2d-matrix-ii/) lo = start; hi = len(matrix[0]) - 1 if vertical else len(matrix) - 1; while hi >= lo: mid = (lo + hi) // 2
    - the fact that the matrix is sorted suggests that there must be some way to use binary search to speed up our algorithm.
  -

- Approach: Divide and Conquer
 - [240](https://leetcode.com/problems/search-a-2d-matrix-ii/) def search_rec(left, up, right, down):
  - For a matrix, the left-up is smallest, while the bottom-right is largest
 - []


# Functions

### List

    | Description             | Function-1                  | Function-2                     |       Function-3 |
    |-------------------------|-----------------------------|--------------------------------|------------------|
    | sort the list           | xxx.sort()                  | sorted(xxx)                    |                  |
    | sort a list of lists    | xxx.sort(key=lambda x:x[0]) | sorted(xxx, key=lambda x: x[0])|                  |
    | sort a list of lists based on a second list |  [x for _, x in sorted(zip(yyy, xxx))] | |                  |
    | insert items to list    | xxx.append(value)           | xxx.insert(index, value)       | xxx.extend(list) |
    | insert lists to list    | xxx.append(list)            | xxx.insert(index, list)        |                  |
    | delete items from list  | xxx.remove(value)           | xxx.pop(index)                 | del xxx[index]   |

### Set
    | Description             | Function-1        | Function-2               |
    |-------------------------|-------------------|--------------------------|
    | set: s belongs to t     | s.issubset(t)     | s <= t                   |                  
    | set: union              | s.union(t)        | s \| t                   |                  
    | set: intersection       | s.intersection(t) | s & t                    |                  
    | set: x in s but not in t| s.diference(t)    | s - t                    |                  

### string
    | Description                        | Function-1                        | Function-2                              |
    |------------------------------------|-----------------------------------|-----------------------------------------|
    | return index of "chars" in string  | s.find("chars") from left to right|  s.rfind("charts"), from right to left  |                
    | split a string to a list of letters| s.split()                         |                                         |
    | join a list of strings to one      | " ".join(s_list)                  |                                         |

### Package: colletions

| Description                        | Function-1                                                                     |
|------------------------------------|--------------------------------------------------------------------------------|
| _dict = collections.Counter(nums)  | collections.Counter("Hello") = Counter({'l': 2, 'H': 1, 'e': 1, 'o': 1})       |
