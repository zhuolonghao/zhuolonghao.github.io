---
layout: post
title: "[Coding] Data Structure: List"
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

- Approach: Sliding Window, time complexity = O(n)
  - [487](https://leetcode.com/problems/max-consecutive-ones-ii/):longest_sequence=0, left, right = 0, 0, num_zeroes=0, while right < len(nums):  

- Approach: Set
  - [414](https://leetcode.com/problems/third-maximum-number/): set(nums), .remove(), .remove(), .remove()
  - [448](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/): set operation: set() - set()

# Functions

    | Description             | Function-1        | Function-2               |       Function-3 |
    |-------------------------|-------------------|--------------------------|------------------|
    | sorting the list        | xxx.sort()        | sorted(xxx)              |                  |
    | inserting items to list | xxx.append(value) | xxx.insert(index, value) | xxx.extend(list) |
    | deleting items from list| xxx.remove(value) | xxx.pop(index)           | del xxx[index]   |
