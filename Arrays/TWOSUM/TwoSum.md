# Two Sum Problem

## Description

Given an array of integers `nums` and an integer `target`, find two numbers such that they add up to the `target`. Return the indices of the two numbers as an array.

Assume that each input has exactly one solution, and the same element cannot be used twice.

## Example

### Example 1

Input: `nums = [2,7,11,15]`, `target = 9`

Output: `[0,1]`

Explanation: `nums[0] + nums[1] == 9`, so we return `[0, 1]`.

### Example 2

Input: `nums = [3,2,4]`, `target = 6`

Output: `[1,2]`

### Example 3

Input: `nums = [3,3]`, `target = 6`

Output: `[0,1]`

## Constraints

- `2 <= nums.length <= 10^4`
- `-10^9 <= nums[i] <= 10^9`
- `-10^9 <= target <= 10^9`
- Only one valid answer exists.

## Follow-up

Can you come up with an algorithm that is less than O(n^2) time complexity?

## Implementation

### Language

Choose your preferred programming language (e.g., Python, C++).

### Function Signature

# For C++
std::vector<int> twoSum(std::vector<int>& nums, int target) {
    // Your implementation here
}

