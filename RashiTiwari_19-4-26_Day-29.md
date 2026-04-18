Problem Statement- Fibonacci Number
code:
class Solution {
public:

    int fib(int n) {
        if (n == 0) return 0;
        if (n == 1) return 1;

        int a = 0, b = 1, c;
        for (int i = 2; i <= n; i++) {
            c = a + b;
            a = b;
            b = c;
        }
        return b;
    }
};

screenshot:
<img width="1691" height="770" alt="Screenshot 2026-04-19 001743" src="https://github.com/user-attachments/assets/8035aecf-6c16-4469-bdd5-b2f9a00ecce0" />
