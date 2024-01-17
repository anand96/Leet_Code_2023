# Subsets

https://leetcode.com/problems/subsets/description/

Solution Reference :

https://www.hackerearth.com/practice/basic-programming/bit-manipulation/basics-of-bit-manipulation/tutorial/

Given an integer array nums of unique elements, return all possible 
subsets
 (the power set).

The solution set must not contain duplicate subsets. Return the solution in any order.

## Example 1:

Input: nums = [1,2,3]
Output: [[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3]]

## Example 2:

Input: nums = [0]
Output: [[],[0]]
 
## Constraints:

1 <= nums.length <= 10
-10 <= nums[i] <= 10
All the numbers of nums are unique.


## Solution 

```
class Solution {
    public List<List<Integer>> subsets(int[] nums) {
        List<List<Integer>> solution = new ArrayList<>();
        int len = nums.length;
        for(int i=0;i<(1 << len); ++i)
        {
            List<Integer> inner = new ArrayList<>();
            for(int j=0; j < len; ++j)
            {    
                if((i & (1<<j))!=0)
                    inner.add(nums[j]);
            }
            solution.add(inner);
        }
        return solution;
    }
}
```
