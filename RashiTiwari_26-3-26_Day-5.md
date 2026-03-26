Problem Statement - MOVE ZEROES

Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.
Note that you must do this in-place without making a copy of the array.

CODE - class Solution {
public:

    void moveZeroes(vector<int>& nums) {
        int n= nums.size();
        int indexpos=0;
        int i=0;
        for(int i=0;i<n;i++){
          if(nums[i]!=0){
            nums[indexpos]=nums[i];
            indexpos++;
         }
        }
         for (int i=indexpos;i<n;i++) {
        nums[i]=0;
    }
    for(int x:nums){
        cout<< x<< " ";
    }
    cout << endl;
    
    }
};


ScreenShot - 
<img width="1837" height="825" alt="Screenshot 2026-03-26 113602" src="https://github.com/user-attachments/assets/d29acfe7-274a-410e-8ca5-d2cbd3884ffc" />

