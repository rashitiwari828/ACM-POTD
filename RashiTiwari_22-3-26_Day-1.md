Problem statement - Remove duplicates from sorted array

Solution-

class Solution {
public:
    int removeDuplicates(vector<int>& nums) {
        if (nums.empty()) return 0;

        int k = 1;  // first element is always unique
        for (int i = 1; i < nums.size(); i++) {
            if (nums[i] != nums[k - 1]) {
                nums[k] = nums[i];  // place unique element at position k
                k++;
            }
        }
        return k;
    }
};

Screenshot-
<img width="1899" height="827" alt="Screenshot 2026-03-22 145521" src="https://github.com/user-attachments/assets/17ff6fb4-c100-4660-b1a4-a45156ebe0fb" />

