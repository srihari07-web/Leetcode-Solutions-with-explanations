# Two Sum Problem - Two Pointers Approach

## Description

This implementation provides a solution to the Two Sum problem using the Two Pointers approach. Given an array of integers `nums` and an integer `target`, the goal is to find two numbers in the array that add up to the target and return their indices.

## Approach Explanation

1. **Create Pairs with Original Indices:**
   - To keep track of the original indices, create a vector of pairs named `arr`. Each pair consists of a number from the `nums` array and its original index, achieved using `make_pair(nums[i], i)`.
   

2. **Sort the Vector:**
   - Sort the `arr` vector based on the numbers (the first element of each pair). Sorting is essential for the Two Pointers approach.

3. **Two Pointers Approach:**
   - Initialize two pointers, `left` and `right`, at the beginning and end of the sorted vector, respectively.
   - Use a while loop to iterate through the array:
     - If the sum of the numbers at the current pointers is greater than the target, decrement the `right` pointer.
     - If the sum is less than the target, increment the `left` pointer.
     - If the sum equals the target, return the original indices corresponding to the numbers found.

4. **No Solution Found:**
   - If the while loop completes without finding a valid pair, return an empty vector `{0, 0}`, indicating no valid solution.

## Implementation

```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int n = nums.size();
        vector<pair<int, int>> arr;

        // Create a vector of pairs (number, original index)
        for (int i = 0; i < n; i++) {
            arr.push_back(make_pair(nums[i], i));
        }

        // Sort the vector based on the numbers
        sort(arr.begin(), arr.end());

        int left = 0, right = n - 1;

        // Two Pointers Movement
        while (left < right) {
            if (arr[left].first + arr[right].first > target) {
                right--;
            } else if (arr[left].first + arr[right].first < target) {
                left++;
            } else {
                // Return the original indices
                return {arr[left].second, arr[right].second};
            }
        }

        // No Solution Found
        return {0, 0};
    }
};
