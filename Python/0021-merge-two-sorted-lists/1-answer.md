# [Header](link)

## 🧑🏻‍💻 Approach
<!-- Describe your approach to solving the problem. -->
Explain the approach

## 🔐 Code

``` python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def mergeTwoLists(self, list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
        if not list1:
            return list2
        if not list2:
            return list1

        dummy = ListNode()
        resultCurr = dummy

        curr1 = list1
        curr2 = list2

        while curr1 and curr2:
            if curr1.val < curr2.val:
                resultCurr.next = curr1
                curr1 = curr1.next
            else: 
                resultCurr.next = curr2
                curr2 = curr2.next

            resultCurr = resultCurr.next

        resultCurr.next = curr1 if curr1 is not None else curr2
        
        return dummy.next
```

## 🧩 Complexity

- Time complexity:
<!-- Add your time complexity here, e.g. $O(n)$ -->
Time Complexity

- Space complexity:
<!-- Add your space complexity here, e.g. $O(n)$ -->
Space Complexity
