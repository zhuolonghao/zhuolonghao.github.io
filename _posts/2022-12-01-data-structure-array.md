  ---
layout: post
title: "[Coding] Data Structure: List and String"
---

{{ page.title }}
================

<p class="meta">Dec 2022 - Charlotte, NC</p>

# By Topic

### String
- [5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/): A palindrome is a string which reads the same in both directions. E.g., S = "aba" is a palindrome, SS = "abc" is not.

- [1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/): A common subsequence is a sequence of letters that appears in both strings by its order. E.g., s1 = "acde", s2 = "ace", ans = "ace". Noted it's different from the substring (should be "ac" only).  

- [187. Repeated DNA Sequences](https://leetcode.com/problems/repeated-dna-sequences/)
  - Rabin-Karp: the idea is slice over the string and to compute the hash (i.e., a series of numeric numbers representing a symbol) of the sequence in the sliding window, both in a constant time.
    - initial hash ```for i in range(L):  h = h * a + nums[i]```
    - rolling hash ```h = h * a - nums[start - 1] * aL + nums[start + L - 1]```
    - rolling hash parameter: ``` a = 4; aL = pow(a, L)```
    - string conversion: ```to_int = {'A': 0, 'C': 1, 'G': 2, 'T': 3};  nums = [to_int.get(s[i]) for i in range(n)]```

- [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/): find the longest common prefix string amongst multiple strings.
  - vertical scan: assume the str[0] is the answer, scan other strings and trim accordingly
  - Divide-Conquer: divide multiple strings to pairwise strings and compare.  
  - Binary Search: assume the str[0] is the answer, split letters in the string to half, and search if pattern is matched.

### Array

# By Approach

### Greedy Algorithm

- [763. Partition Labels](https://leetcode.com/problems/partition-labels/)
  - pattern: for each letter encountered, process the last occurrence of that letter,  extending the current partition ```[anchor, j]``` *appropriately*.
``` python
last = {c: i for i, c in enumerate(S)}
j = anchor = 0
ans = []
for i, c in enumerate(S):
      j = max(j, last[c])
      if i == j: # j marks the last occurrence of all letters previously seen.
        ans.append(i - anchor + 1)
        anchor = i + 1
```

### Divide and Conquer

- [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
  - Divide until there're two strings left, lcp_left and lcp_right, and then call the conquer function.
```python
def Divide(strs: List[str], left_index, right_index) -> str:
      if left_index == right_index:
          return strs[right_index]

      mid = (left_index + right_index)//2
      lcp_left = Solution.Divide(strs, left_index, mid)
      lcp_right = Solution.Divide(strs, mid + 1, right_index)
      return Solution.conquer(lcp_left, lcp_right)
```
  - Conquer: find the common substring between two strings
```python
def conquer(left_string, right_string):
      for i, (l, r) in enumerate(zip(left_string, right_string)):
          if l != r:
              return left_string[:i]
      return min(left_string, right_string, key=len)
```
  - Wrapper:
  ```python
  def longestCommonPrefix(self, strs: List[str]) -> str:
      if not strs:
          return ""
      return Solution.Divide(strs, 0, len(strs) - 1)
  ```

### Hash Table

- [187. Repeated DNA Sequences](https://leetcode.com/problems/repeated-dna-sequences/)
 ``` python
 ans = set()
 if sub not in ans:  ans[sub] = 1; else: ans[sub] += 1;
```

- [49. Group Anagrams](https://leetcode.com/problems/group-anagrams/): An Anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once.  Note [list unhashable, but tuple hashable.](https://stackoverflow.com/questions/37136878/list-unhashable-but-tuple-hashable)
``` python
ans = collections.defaultdict(list)
ans[tuple(sorted(s))].append(s)
```

- [763. Partition Labels](https://leetcode.com/problems/partition-labels/)
``` python
_count = collections.Counter(S)
_dict, cnt, ans = {}, 0, []
for i in range(len(S)):
    cnt += 1
    if S[i] not in _dict:
        _dict[S[i]] = _count[S[i]]
    _dict[S[i]] -= 1
    if all(v == 0 for v in _dict.values()):
        ans.append(cnt)
        _dict, cnt = {}, 0
```

### Dynamic Programming

- [5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
  - longest common substrings:
    - set a space for dp: ```dp = [ [0] * (n+1) for _ in range(n+1)] ```
    - define carry:
    ``` python
    for i in range(n+1):
        for j in range(n+1):
            if (i==0) | (j==0):
                dp[i][j] = 0
            elif s[i-1] == s_rev[j-1]:
                dp[i][j] = 1 + dp[i-1][j-1]
    ```
    - output: ```ans = s[(i-dp[i][j]):i]```
  - another idea of implementing dynamic programing:
    - set a space for dp: ```dp = [ [0] * (n) for _ in range(n)]```
    - define carry:
    ``` python      
    for i in range(1, n):
        dp[i][i] = 1
    ans = s[0]
    for j in range(1, n):
        for i in range(j):
            if (s[i] == s[j]) & ( (dp[i+1][j-1] == 1) | (i+1 == j)):
                dp[i][j] = 1
    ```
    - output: ```ans = s[i:j+1]```

- [1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)
  - DP, traditional
    - set a space for dp: ``` dp = [[0]* (ncol+1) for _ in range(nrow+1)] ```
    - define carry and output:  
    ```python
    for i in range(nrow+1):
        for j in range(ncol+1):
          if (i == 0) | (j == 0):
              dp[i][j] == 0
          elif short[i-1] == long[j-1]:
              dp[i][j] = 1 + dp[i-1][j-1]
              cnt = max(cnt, dp[i][j])
          else:
              # this is crucial as it brings the previous information forward.
              dp[i][j] = max(dp[i][j-1], dp[i-1][j])
    ```
  - DP, Space Optimization
    - find a structure for dp set-up:
    ```python
    if len(text2) < len(text1):
            text1, text2 = text2, text1
    previous = [0] * (len(text1) + 1);
    current = [0] * (len(text1) + 1)
    ```
    - define carry
    ``` python
    for col in reversed(range(len(text2))):
      for row in reversed(range(len(text1))):
        if text2[col] == text1[row]:
          current[row] = 1 + previous[row + 1]
        else:
          current[row] = max(previous[row], current[row + 1])  
        previous, current = current, previous
    ```

- [43. Multiply Strings](https://leetcode.com/problems/multiply-strings/)
  - set a space for dp: ``` N = len(num1) + len(num2); answer = [0] * N ```
  - define carry:
  ``` python
  first_number = num1[::-1]
  second_number = num2[::-1]
  for place2, digit2 in enumerate(second_number):
      for place1, digit1 in enumerate(first_number):
          num_zeros = place1 + place2
          carry = answer[num_zeros]
          multiplication = int(digit1) * int(digit2) + carry
          answer[num_zeros] = multiplication % 10
          answer[num_zeros + 1] += multiplication // 10
  ```

- [152. Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
  - set initial dp: ```max_so_far = nums[0]; min_so_far = nums[0]; result = max_so_far```
  - define carry:
  ```python
  for i in range(1, len(nums)):
      curr = nums[i]
      # Carry starts from here
      temp_max = max(curr, max_so_far * curr, min_so_far * curr)
      min_so_far = min(curr, max_so_far * curr, min_so_far * curr)
      # Carry Ends here
      max_so_far = temp_max
      result = max(max_so_far, result)
  ```


### Two Pointers

- [344. Reverse String](https://leetcode.com/problems/reverse-string/)
``` python
left, right = 0, len(s) - 1
while left < right:
    s[left], s[right] = s[right], s[left]
    left, right = left + 1, right - 1
```

- [209. Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/)
```python
left, right =0, 0
_sum, cnt = math.inf, 0
while(right<len(nums)):
    _sum=_sum+nums[p2]
    if _sum<target:
        right += 1
    else:
        cnt  = min(cnt, right - left + 1)
        # Need to walk back nums[right]
        _sum = _sum-nums[left]-nums[right]
        left+= 1
```

### Binary Search

- [14. Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
  ```python
    left_index  = 1
    right_index = min([len(i) for i in strs])
    while left_index <= right_index:
        middle = (left_index + right_index)//2
        # below decides the position of next binary cut
        if isCommonPrefix(strs, middle):  
            left_index = middle + 1
        else:
            right_index = middle - 1
  ```

- [209. Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/)
  ```python
  n, cnt = len(nums), math.inf
  sums = [0]*(n+1)
  for i in range(1, n+1):
      sums[i] = sums[i-1]+nums[i-1]
  for l in range(1, n+1):
      r = bisect_left(sums, target+sums[l-1])
      # bisect_left does the job below
      # find the rightmost index at which the value is less than target+sums[l-1]
      # for i in range(n):
      #   if (sums[i] - target) <= sums[l-1]:
      #     r = i
      #     break
      if r < n+1:
          min_ = min(min_, r-l+1)
  ```


### Recursive Programming

- [1143. Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)



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
| return the idx of a given input such that it splits the sorted list| bisect_left(List, value)| bisect.bisect_left([1,2,3], 2) ---> 1 |
| return the idx of a given input such that it splits the sorted list| bisect_right(List, value)| bisect.bisect_right([1,2,3], 2) ---> 2|

### Set
| Description             | Function-1        | Function-2               |
|-------------------------|-------------------|--------------------------|
| set: s belongs to t | s.issubset(t)     | s <= t                   |                  
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

### Package: colletions

| Functions                          | Outcome or Description                                                         |
|------------------------------------|--------------------------------------------------------------------------------|
| _dict = collections.Counter(nums)  | collections.Counter("Hello") = Counter({'l': 2, 'H': 1, 'e': 1, 'o': 1})       |
| _dict = collections.defaultdict(int) | create a dictionary whose values are integer |
| _dict = collections.defaultdict(list) | create a dictionary whose values are list   |














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
