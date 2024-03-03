# [Header](link)

## 🧑🏻‍💻 Approach
<!-- Describe your approach to solving the problem. -->
Explain the approach

## 🔐 Code

``` python
class Solution:
    def search(self, nums: List[int], target: int) -> int:
        left = 0
        right = len(nums) - 1

        while left <= right:
            middle = (left + right) // 2 

            if nums[middle] == target:
                return middle 
            
            if nums[middle] > target:
                right = middle - 1  
            else:
                left = middle + 1 

        return -1 
```

## 🧩 Complexity

- Time complexity:
<!-- Add your time complexity here, e.g. $O(n)$ -->
Time Complexity

- Space complexity:
<!-- Add your space complexity here, e.g. $O(n)$ -->
Space Complexity
