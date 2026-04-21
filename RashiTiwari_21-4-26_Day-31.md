Problem statement - climbing stairs

code:
class Solution {
public:

    int climbStairs(int n) {
        if (n <= 2) return n;   
        int a = 1, b = 2;      
        for (int i = 3; i <= n; i++) {
            int c = a + b;     
            a = b;
            b = c;
        }
        return b;
    }
};

screenshot:
<img width="1519" height="842" alt="Screenshot 2026-04-21 065510" src="https://github.com/user-attachments/assets/6c72b9e8-3e0a-46e7-8d30-460151cd2580" />
