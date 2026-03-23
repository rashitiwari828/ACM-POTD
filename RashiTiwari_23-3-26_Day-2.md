Problem Statement - TWO SUM
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

Solution- 
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
    
        unordered_map<int, int> hashmap; 
        for (int i = 0; i < nums.size(); i++) {
            int diff = target - nums[i];
            if (hashmap.find(diff) != hashmap.end()) {
                return {hashmap[diff], i};
            }
            hashmap[nums[i]] = i;
        }
        return {};
    }
};

 ScreenShot - 
 
<img width="1884" height="854" alt="Screenshot 2026-03-23 191450" src="https://github.com/user-attachments/assets/957e67d3-7e6b-4460-b9fc-94a60bf5509d" />
