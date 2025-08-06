

---

### 🔹**Question 1: Find Maximum in Array**

**Problem:**

Given an array of integers, find and return the maximum element in the array.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `[1, 2, 3, 4, 5]`
Output: `5`

**Test Case 2:**
Input: `[-1, -2, -3, -4]`
Output: `-1`

**Test Case 3:**
Input: `[5]`
Output: `5`

**Test Case 4:**
Input: `[0, 100, -100, 99]`
Output: `100`

**Test Case 5:**
Input: `[10, 9, 8, 7, 6]`
Output: `10`

---

### 🔹**Solution:**

```python
class Solution:
    def findMaximum(self, nums):
        max_val = nums[0]
        for num in nums:
            if num > max_val:
                max_val = num
        return max_val

# Driver code
if __name__ == "__main__":
    n = int(input())  # Length of the array
    nums = []
    for _ in range(n):
        val = int(input())
        nums.append(val)

    obj = Solution()
    print(obj.findMaximum(nums))
```

---

---

### 🔹**Question 2: Find First Occurrence of Element**

**Problem:**

Given an array of integers and a target value, find and return the **first index** where the target appears. If the target is not present, return `-1`.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i], target ≤ 10⁵

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `[1, 2, 3, 4, 5]`, Target: `3`
Output: `2`

**Test Case 2:**
Input: `[5, 1, 2, 3, 5]`, Target: `5`
Output: `0`

**Test Case 3:**
Input: `[7, 8, 9]`, Target: `6`
Output: `-1`

**Test Case 4:**
Input: `[1]`, Target: `1`
Output: `0`

**Test Case 5:**
Input: `[10, 20, 30, 10, 20]`, Target: `20`
Output: `1`

---

### 🔹**Solution:**

```python
class Solution:
    def firstOccurrence(self, nums, target):
        for i in range(len(nums)):
            if nums[i] == target:
                return i
        return -1

# Driver code
if __name__ == "__main__":
    n = int(input())  # Length of the array
    nums = []
    for _ in range(n):
        val = int(input())
        nums.append(val)
    target = int(input())  # Target value to search

    obj = Solution()
    print(obj.firstOccurrence(nums, target))
```

---

---

### 🔹**Question 3: Find First Occurrence of Element**

**Problem:**

Given an array of integers and a target value `x`, return the **index of the first occurrence** of `x` in the array. If `x` is not found, return `-1`.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i], x ≤ 10⁵

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `arr = [1, 2, 3, 4, 5], x = 3`
Output: `2`

**Test Case 2:**
Input: `arr = [5, 4, 3, 2, 1], x = 4`
Output: `1`

**Test Case 3:**
Input: `arr = [10, 20, 30, 40, 50], x = 100`
Output: `-1`

**Test Case 4:**
Input: `arr = [1, 2, 2, 2, 3], x = 2`
Output: `1`

**Test Case 5:**
Input: `arr = [7], x = 7`
Output: `0`

---

### 🔹**Solution:**

```python
class Solution:
    def findFirstIndex(self, nums, x):
        for i in range(len(nums)):
            if nums[i] == x:
                return i
        return -1

# Driver code
if __name__ == "__main__":
    n = int(input())  # Length of the array
    nums = []
    for _ in range(n):
        val = int(input())
        nums.append(val)
    x = int(input())  # Element to find

    obj = Solution()
    print(obj.findFirstIndex(nums, x))
```

---

### 🔹**Question 4: Check if Array is Sorted (Strictly Increasing)**

**Problem:**

Given an array of integers, check whether the array is sorted in strictly increasing order. That means every element must be less than the next one.

Return `True` if the array is strictly increasing, otherwise return `False`.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `arr = [1, 2, 3, 4, 5]`
Output: `True`

**Test Case 2:**
Input: `arr = [5, 4, 3, 2, 1]`
Output: `False`

**Test Case 3:**
Input: `arr = [1, 2, 2, 3]`
Output: `False`

**Test Case 4:**
Input: `arr = [10]`
Output: `True`

**Test Case 5:**
Input: `arr = [-3, -2, -1, 0, 1]`
Output: `True`

---

### 🔹**Solution:**

```python
class Solution:
    def isStrictlyIncreasing(self, nums):
        for i in range(1, len(nums)):
            if nums[i] <= nums[i-1]:
                return False
        return True

# Driver code
if __name__ == "__main__":
    n = int(input())  # Length of the array
    nums = []
    for _ in range(n):
        val = int(input())
        nums.append(val)

    obj = Solution()
    print(obj.isStrictlyIncreasing(nums))
```

---
---

### 🔹**Question 5: Find Second Largest Element in Array**

**Problem:**

Given an array of integers, return the second largest unique element in the array. If there is no such element (i.e., all elements are the same or only one element exists), return `-1`.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `arr = [1, 2, 3, 4, 5]`
Output: `4`

**Test Case 2:**
Input: `arr = [5, 5, 5, 5]`
Output: `-1`

**Test Case 3:**
Input: `arr = [10]`
Output: `-1`

**Test Case 4:**
Input: `arr = [10, 20, 10, 20, 30]`
Output: `20`

**Test Case 5:**
Input: `arr = [-1, -2, -3, -4]`
Output: `-2`

---

### 🔹**Solution:**

```python
class Solution:
    def secondLargest(self, nums):
        unique_nums = list(set(nums))
        if len(unique_nums) < 2:
            return -1
        unique_nums.sort(reverse=True)
        return unique_nums[1]

# Driver code
if __name__ == "__main__":
    n = int(input())  # Length of the array
    nums = []
    for _ in range(n):
        val = int(input())
        nums.append(val)

    obj = Solution()
    print(obj.secondLargest(nums))
```

---
---

### 🔹**Question 6: Check Palindrome Number**

**Problem:**

Given an integer `x`, return `True` if `x` is a palindrome integer.
An integer is a palindrome when it reads the same backward as forward.
Negative numbers are **not** palindromes.

**Constraints:**

* -2³¹ ≤ x ≤ 2³¹ − 1

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `x = 121`
Output: `True`

**Test Case 2:**
Input: `x = -121`
Output: `False`

**Test Case 3:**
Input: `x = 10`
Output: `False`

**Test Case 4:**
Input: `x = 0`
Output: `True`

**Test Case 5:**
Input: `x = 12321`
Output: `True`

---

### 🔹**Solution:**

```python
class Solution:
    def isPalindrome(self, x: int) -> bool:
        if x < 0:
            return False
        return str(x) == str(x)[::-1]

# Driver code
if __name__ == "__main__":
    x = int(input())  # Single integer input
    obj = Solution()
    print(obj.isPalindrome(x))
```

---
---

### 🔹**Question 7: Find the Majority Element**

**Problem:**

Given an array `nums` of size `n`, return **the majority element**.
The majority element is the element that appears **more than ⌊n / 2⌋ times**.
You may assume that the majority element **always exists** in the array.

**Constraints:**

* `n == nums.length`
* `1 <= n <= 5 * 10⁴`
* `-10⁹ <= nums[i] <= 10⁹`

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `nums = [3,2,3]`
Output: `3`

**Test Case 2:**
Input: `nums = [2,2,1,1,1,2,2]`
Output: `2`

**Test Case 3:**
Input: `nums = [1]`
Output: `1`

**Test Case 4:**
Input: `nums = [1,1,1,2,3,4,1]`
Output: `1`

**Test Case 5:**
Input: `nums = [7,7,5,7,5,1,7]`
Output: `7`

---

### 🔹**Solution:**

```python
class Solution:
    def majorityElement(self, nums: list[int]) -> int:
        count = 0
        candidate = None

        for num in nums:
            if count == 0:
                candidate = num
            count += (1 if num == candidate else -1)

        return candidate

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))  # Space-separated integers
    obj = Solution()
    print(obj.majorityElement(nums))
```

---
---

### 🔹**Question 8: Count Occurrences of a Number in Array**

**Problem:**

Given an array of integers and a target number `x`, return the number of times `x` occurs in the array.

**Constraints:**

* 1 ≤ length of array ≤ 10⁴
* -10⁵ ≤ array\[i], x ≤ 10⁵

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `nums = [1, 2, 2, 3, 4], x = 2`
Output: `2`

**Test Case 2:**
Input: `nums = [1, 1, 1, 1], x = 1`
Output: `4`

**Test Case 3:**
Input: `nums = [5, 6, 7, 8], x = 9`
Output: `0`

**Test Case 4:**
Input: `nums = [0, -1, -1, 0], x = -1`
Output: `2`

**Test Case 5:**
Input: `nums = [3], x = 3`
Output: `1`

---

### 🔹**Solution:**

```python
class Solution:
    def countOccurrences(self, nums: list[int], x: int) -> int:
        count = 0
        for num in nums:
            if num == x:
                count += 1
        return count

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))  # Space-separated integers
    x = int(input())  # Element to count
    obj = Solution()
    print(obj.countOccurrences(nums, x))
```

---
---

### 🔹**Question 9: Find the Missing Number from 0 to n**

**Problem:**

Given an array `nums` containing `n` distinct numbers in the range `[0, n]`, return the **missing number**.

**Constraints:**

* `n == nums.length`
* `1 <= n <= 10⁴`
* `0 <= nums[i] <= n`
* All the numbers of the array are unique and exactly one number is missing in the range `[0, n]`

---

### 🔹**Example Test Cases:**

**Test Case 1:**
Input: `nums = [3, 0, 1]`
Output: `2`

**Test Case 2:**
Input: `nums = [0, 1]`
Output: `2`

**Test Case 3:**
Input: `nums = [9,6,4,2,3,5,7,0,1]`
Output: `8`

**Test Case 4:**
Input: `nums = [1]`
Output: `0`

**Test Case 5:**
Input: `nums = [0, 2]`
Output: `1`

---

### 🔹**Solution:**

```python
class Solution:
    def missingNumber(self, nums: list[int]) -> int:
        n = len(nums)
        total = n * (n + 1) // 2
        return total - sum(nums)

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))  # Space-separated integers
    obj = Solution()
    print(obj.missingNumber(nums))
```

---
---

### 🔹**Question 10: Reverse the Array**

**Problem:**

Given an array of integers, reverse the array **in-place** and return it.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `arr = [1, 2, 3, 4, 5]`
Output: `[5, 4, 3, 2, 1]`

**Test Case 2:**
Input: `arr = [10]`
Output: `[10]`

**Test Case 3:**
Input: `arr = [7, -8, 9]`
Output: `[9, -8, 7]`

**Test Case 4:**
Input: `arr = []`
Output: `[]`

**Test Case 5:**
Input: `arr = [-1, 0, 1]`
Output: `[1, 0, -1]`

---

**Solution:**

```python
class Solution:
    def reverseArray(self, nums):
        left, right = 0, len(nums) - 1
        while left < right:
            nums[left], nums[right] = nums[right], nums[left]
            left += 1
            right -= 1
        return nums

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.reverseArray(nums))
```

---

### 🔹**Question 11: Sum of Elements in Array**

**Problem:**

Given an array, return the sum of all its elements.

**Constraints:**

* 1 ≤ length of array ≤ 10⁴
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `arr = [1, 2, 3]`
Output: `6`

**Test Case 2:**
Input: `arr = [-1, -2, -3]`
Output: `-6`

**Test Case 3:**
Input: `arr = [0, 0, 0]`
Output: `0`

**Test Case 4:**
Input: `arr = [100, 200]`
Output: `300`

**Test Case 5:**
Input: `arr = [10]`
Output: `10`

---

**Solution:**

```python
class Solution:
    def sumArray(self, nums):
        return sum(nums)

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.sumArray(nums))
```

---

### 🔹**Question 12: Count Even Numbers in Array**

**Problem:**

Given an array, count how many elements are even.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `arr = [1, 2, 3, 4]`
Output: `2`

**Test Case 2:**
Input: `arr = [1, 3, 5]`
Output: `0`

**Test Case 3:**
Input: `arr = [2, 4, 6, 8]`
Output: `4`

**Test Case 4:**
Input: `arr = [0]`
Output: `1`

**Test Case 5:**
Input: `arr = [-2, -4, 3, 7]`
Output: `2`

---

**Solution:**

```python
class Solution:
    def countEvens(self, nums):
        count = 0
        for num in nums:
            if num % 2 == 0:
                count += 1
        return count

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.countEvens(nums))
```

---

### 🔹**Question 13: Check if Element Exists**

**Problem:**

Given an array and an integer `x`, return `True` if `x` exists in the array, else `False`.

**Constraints:**

* 1 ≤ length of array ≤ 10⁴
* -10⁵ ≤ array\[i], x ≤ 10⁵

---

**Test Case 1:**
Input: `arr = [1, 2, 3], x = 2`
Output: `True`

**Test Case 2:**
Input: `arr = [4, 5, 6], x = 7`
Output: `False`

**Test Case 3:**
Input: `arr = [10], x = 10`
Output: `True`

**Test Case 4:**
Input: `arr = [1, 2, 3, 4], x = 0`
Output: `False`

**Test Case 5:**
Input: `arr = [-3, -2, -1], x = -2`
Output: `True`

---

**Solution:**

```python
class Solution:
    def exists(self, nums, x):
        return x in nums

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    x = int(input())
    obj = Solution()
    print(obj.exists(nums, x))
```

---

---

### 🔹**Question 14: Find the Minimum Element in Array**

**Problem:**

Given an array of integers, find and return the minimum element.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `[1, 2, 3, 4]`
Output: `1`

**Test Case 2:**
Input: `[-1, -2, -3]`
Output: `-3`

**Test Case 3:**
Input: `[10]`
Output: `10`

**Test Case 4:**
Input: `[0, 100, -200, 50]`
Output: `-200`

**Test Case 5:**
Input: `[3, 3, 3]`
Output: `3`

---

**Solution:**

```python
class Solution:
    def findMinimum(self, nums):
        min_val = nums[0]
        for num in nums:
            if num < min_val:
                min_val = num
        return min_val

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.findMinimum(nums))
```

---

### 🔹**Question 15: Remove Duplicates from Array**

**Problem:**

Given an array of integers, return a new list with duplicates removed (order doesn't matter).

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `[1, 2, 2, 3]`
Output: `[1, 2, 3]`

**Test Case 2:**
Input: `[5, 5, 5]`
Output: `[5]`

**Test Case 3:**
Input: `[1, 2, 3]`
Output: `[1, 2, 3]`

**Test Case 4:**
Input: `[10, 10, 20, 30]`
Output: `[10, 20, 30]`

**Test Case 5:**
Input: `[-1, -2, -1, -3]`
Output: `[-1, -2, -3]`

---

**Solution:**

```python
class Solution:
    def removeDuplicates(self, nums):
        return list(set(nums))

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.removeDuplicates(nums))
```

---

### 🔹**Question 16: Count Positive Numbers in Array**

**Problem:**

Given an array of integers, count how many numbers are **greater than 0**.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `[1, -1, 2, -2, 0]`
Output: `2`

**Test Case 2:**
Input: `[-5, -3, -1]`
Output: `0`

**Test Case 3:**
Input: `[10, 20, 30]`
Output: `3`

**Test Case 4:**
Input: `[0, 0, 0]`
Output: `0`

**Test Case 5:**
Input: `[5]`
Output: `1`

---

**Solution:**

```python
class Solution:
    def countPositive(self, nums):
        count = 0
        for num in nums:
            if num > 0:
                count += 1
        return count

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.countPositive(nums))
```

---

### 🔹**Question 17: Find the Index of the Last Occurrence**

**Problem:**

Given an array and a target number `x`, return the **last index** where `x` occurs. If not found, return `-1`.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i], x ≤ 10⁵

---

**Test Case 1:**
Input: `arr = [1, 2, 3, 2], x = 2`
Output: `3`

**Test Case 2:**
Input: `arr = [1, 2, 3], x = 4`
Output: `-1`

**Test Case 3:**
Input: `arr = [5, 5, 5], x = 5`
Output: `2`

**Test Case 4:**
Input: `arr = [0], x = 0`
Output: `0`

**Test Case 5:**
Input: `arr = [7, 8, 9, 8], x = 8`
Output: `3`

---

**Solution:**

```python
class Solution:
    def lastOccurrence(self, nums, x):
        for i in range(len(nums)-1, -1, -1):
            if nums[i] == x:
                return i
        return -1

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    x = int(input())
    obj = Solution()
    print(obj.lastOccurrence(nums, x))
```

---

### 🔹**Question 18: Check if Array Contains Only Zeros**

**Problem:**

Given an array, check whether all elements are zero.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `[0, 0, 0]`
Output: `True`

**Test Case 2:**
Input: `[0, 1, 0]`
Output: `False`

**Test Case 3:**
Input: `[1, 2, 3]`
Output: `False`

**Test Case 4:**
Input: `[0]`
Output: `True`

**Test Case 5:**
Input: `[-1, 0]`
Output: `False`

---

**Solution:**

```python
class Solution:
    def onlyZeros(self, nums):
        for num in nums:
            if num != 0:
                return False
        return True

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.onlyZeros(nums))
```

---

### 🔹**Question 19: Check if All Elements Are Unique**

**Problem:**

Given an array, return `True` if all elements are **unique**, else return `False`.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -10⁵ ≤ array\[i] ≤ 10⁵

---

**Test Case 1:**
Input: `[1, 2, 3]`
Output: `True`

**Test Case 2:**
Input: `[1, 2, 2]`
Output: `False`

**Test Case 3:**
Input: `[10]`
Output: `True`

**Test Case 4:**
Input: `[5, 5, 5, 5]`
Output: `False`

**Test Case 5:**
Input: `[-1, -2, -3, -4]`
Output: `True`

---

**Solution:**

```python
class Solution:
    def areElementsUnique(self, nums):
        return len(set(nums)) == len(nums)

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.areElementsUnique(nums))
```

---

### 🔹**Question 20: Calculate Product of All Elements**

**Problem:**

Given an array, return the product (multiplication) of all elements.

**Constraints:**

* 1 ≤ length of array ≤ 1000
* -100 ≤ array\[i] ≤ 100

---

**Test Case 1:**
Input: `[1, 2, 3]`
Output: `6`

**Test Case 2:**
Input: `[2, 0, 5]`
Output: `0`

**Test Case 3:**
Input: `[-1, 2, -3]`
Output: `6`

**Test Case 4:**
Input: `[10]`
Output: `10`

**Test Case 5:**
Input: `[1, 1, 1, 1]`
Output: `1`

---

**Solution:**

```python
class Solution:
    def productOfArray(self, nums):
        result = 1
        for num in nums:
            result *= num
        return result

# Driver code
if __name__ == "__main__":
    nums = list(map(int, input().split()))
    obj = Solution()
    print(obj.productOfArray(nums))
```

---
