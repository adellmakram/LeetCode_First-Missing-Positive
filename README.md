# LeetCode_First-Missing-Positive

Given an unsorted integer array nums. Return the smallest positive integer that is not present in nums.
You must implement an algorithm that runs in O(n) time and uses O(1) auxiliary space.

 

Example 1:
Input: nums = [1,2,0]
Output: 3
Explanation: The numbers in the range [1,2] are all in the array.

Example 2:
Input: nums = [3,4,-1,1]
Output: 2
Explanation: 1 is in the array but 2 is missing.

Example 3:
Input: nums = [7,8,9,11,12]
Output: 1
Explanation: The smallest positive integer 1 is missing.
 

Constraints:
1 <= nums.length <= 105
-231 <= nums[i] <= 231 - 1


# Solution Description
1. The method initializes an integer x to 1, which represents the starting point for searching the smallest missing positive integer.
2. It creates a HashSet<int> named positiveValues to store the unique positive numbers from the array nums. HashSets are chosen because they efficiently handle uniqueness and allow fast lookups.
3. The method then iterates through each element in the nums array. During each iteration, if an element is positive (greater than 0), it is added to the positiveValues HashSet. This step effectively filters out non-positive numbers and eliminates duplicates.
4. After populating positiveValues, the method iterates, starting from the initial value of x (1), and checks if x is contained within positiveValues. If x is found, it increments x and continues checking the next integer. This process repeats until it encounters the first integer value of x that is not present in positiveValues.
5. Once the loop breaks, the current value of x is the smallest positive integer that is missing from the array, and this value is returned.

# Complexity
- Time complexity:
O(1)

- Space complexity:
O(n)
