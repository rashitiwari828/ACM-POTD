problem statement - Power of two

code:
class Solution {
public:

    bool isPowerOfTwo(int n) {
        return n > 0 && (n & (n - 1)) == 0;
    }
};

screenshot:
<img width="1615" height="777" alt="Screenshot 2026-04-21 065031" src="https://github.com/user-attachments/assets/6fa4ef16-9492-43b7-a542-f817c31679d1" />
