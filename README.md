# Product of array except self
## https://leetcode.com/problems/product-of-array-except-self

Given an array nums of n integers where n > 1,  return an array output such that output[i] is equal to the product of all the elements of nums except nums[i].
```
Example:

Input:  [1,2,3,4]
Output: [24,12,8,6]
Constraint: It's guaranteed that the product of the elements of any prefix or suffix of the array 
(including the whole array) fits in a 32 bit integer.
```
**Note: Please solve it without division and in O(n).**

**Follow up:**
Could you solve it with constant space complexity? (The output array does not count as extra space for the purpose of space complexity analysis.)

# Implementation 1 : Naive
```java
class Solution {
    public int[] productExceptSelf(int[] nums) {
        if(nums == null || nums.length <= 1)
            return nums;
        int[] out = new int[nums.length];
        for(int i = 0; i < nums.length; i++) {
            int product = 1;
            for(int j = 0; j < nums.length; j++) {
                if(i != j)
                    product *= nums[j];
            }
            out[i] = product;
        }
        return out;
    }
}
```

