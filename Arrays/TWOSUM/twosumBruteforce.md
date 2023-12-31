# Two Sum Problem - Brute Force Method

## Description

This implementation provides a brute-force solution to the Two Sum problem. Given an array of integers `nums` and an integer `target`, the goal is to find two numbers in the array that add up to the target and return their indices.

## Brute Force Approach

### Nested Loop Iteration:

- Use two nested loops to iterate through all possible pairs of indices (i, j) in the `nums` array.
- The outer loop (`for i`) represents the first number in the potential pair.
- The inner loop (`for j`) represents the second number in the potential pair and iterates over elements after the current element in the outer loop.

### Pair Check:

- For each pair of indices (i, j), check if the sum of the corresponding numbers (`nums[i] + nums[j]`) is equal to the target value.
- If the sum is equal to the target, return the indices `{i, j}` as the solution.

### No Solution Found:

- If no such pair is found in the nested loops, return an empty result indicating that there is no valid solution.

## Time Complexity

The time complexity of this brute-force approach is O(n^2) because it considers every possible pair of numbers in the array.

## Optimization Opportunity

The brute-force method is straightforward but can be inefficient for large input arrays. A more optimized solution with less than O(n^2) time complexity is possible using hash maps. Consider exploring that approach for improved performance.

## Implementation

```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        for (int i = 0; i < nums.size(); i++) {
            for (int j = i + 1; j < nums.size(); j++) {
                if (nums[i] + nums[j] == target) {
                    return {i, j};
                }
            }
        }

        return {};
    }
};
