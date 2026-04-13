Problem Statement - Find the town judge

code:
class Solution {
public:

    int findJudge(int n, vector<vector<int>>& trust) {
        vector<int> count(n + 1, 0);
         for (auto &t : trust) {
            count[t[0]]--;  
            count[t[1]]++;  
        }
         for (int i = 1; i <= n; i++) {
            if (count[i] == n - 1) return i;
        }
        return -1;
    }
};

Screenshot:<img width="1813" height="800" alt="Screenshot 2026-04-13 225134" src="https://github.com/user-attachments/assets/dfbb49fc-115a-4158-8bf9-eae8d74fe55b" />
