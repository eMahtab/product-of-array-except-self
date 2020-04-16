# Product of array except self
## https://leetcode.com/problems/product-of-array-except-self


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

