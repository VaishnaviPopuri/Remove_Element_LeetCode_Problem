Leetcode Problem 27 - Remove Element

Problem Description

Given an integer array `nums` and an integer `val`, remove all occurrences of `val` in-place.  
The order of the elements may be changed. Then return the number of elements in `nums` which are **not equal** to `val`.

You must:
- Change the array `nums` such that the first `k` elements contain the elements that are not equal to `val`.
- Return `k`.
- The elements beyond `k` are not important.

---

## Examples

### Example 1:
**Input:**  
`nums = [3,2,2,3]`, `val = 3`  
**Output:**  
`2`, `nums = [2,2,_,_]`  
**Explanation:**  
Return `k = 2`. The first two elements of `nums` should be `2`, the rest are ignored.

Example 2:
Input:  
`nums = [0,1,2,2,3,0,4,2]`, `val = 2`  
Output:
`5`, `nums = [0,1,4,0,3,_,_,_]`  
Explanation:
Return `k = 5`. First five elements can be any order of `0,1,3,0,4`.

---

## Constraints

- `0 <= nums.length <= 100`
- `0 <= nums[i] <= 50`
- `0 <= val <= 100`

---

## My Java Solution

```java
public class Solution {
    public int removeElement(int[] nums, int val) 
    {
        int index = 0;
        for (int i = 0; i < nums.length; i++)
        {
            if (nums[i] != val) {
                nums[index] = nums[i];
                index++;
            }
        }
        return index;
    }
}


What I Learned
While solving this problem, I learned the following:

How to iterate through an array using a for loop in Java.

How to compare each element of an array with a given value.

How to overwrite elements in an array to remove unwanted values in-place.

How to use a separate index variable to keep track of the new array length.

The idea of in-place modification without using extra memory or data structures.

Improved my understanding of array manipulation and loop logic in Java.


