Problem Statement- MISSING NUMBER

Given an array nums containing n distinct numbers in the range [0, n], return the only number in the range that is missing from the array

Code- 
class Solution {
public:

    int missingNumber(vector<int>& nums) {
     int n=nums.size();
        int actualSum=0;
        int expectedSum=n*(n+1)/2;
        for(int i=0;i<n;i++){
            actualSum+=nums[i];
                } return expectedSum-actualSum ;
        }

};

ScreenShot- 
<img width="1867" height="780" alt="Screenshot 2026-03-25 155230" src="https://github.com/user-attachments/assets/96a98569-ed73-4263-a55d-91762998af2c" />
