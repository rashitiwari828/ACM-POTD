Problem Statement - Check If N and Its Double Exist

Given an array arr of integers, check if there exist two indices i and j such that :

i != j

0 <= i, j < arr.length

arr[i] == 2 * arr[j]

Code: 
class Solution {
public:

    bool checkIfExist(vector<int>& arr) {
        unordered_set<int> set;
        for (int x : arr) {
            if (set.count(2 * x) || (x % 2 == 0 && set.count(x / 2))) {
                return true;   
            }
            set.insert(x);
        }
        return false;   
    }
};

Screenshot:
<img width="1851" height="767" alt="Screenshot 2026-03-27 192338" src="https://github.com/user-attachments/assets/23e1e8bc-acb3-4391-8940-4e21385062eb" />
