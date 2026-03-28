Problem Statement- 

Rotate Array

Given an integer array nums, rotate the array to the right by k steps, where k is non-negative.

CODE:
class Solution {

public:

    void rotate(vector<int>& nums, int k) {
            int n=nums.size();
            k=k%n;
            reverse(nums.begin(),nums.end());
            reverse(nums.begin(),nums.begin()+k);
            reverse(nums.begin()+k,nums.end());
        
    }
};

SCREENSHOT:
<img width="1848" height="843" alt="Screenshot 2026-03-28 112847" src="https://github.com/user-attachments/assets/864ee524-9d18-4a10-93d2-516a7544d97d" />

