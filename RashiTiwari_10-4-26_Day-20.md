Problem Statement - Remove Outermost Parentheses

code:
class Solution {
public:
    string removeOuterParentheses(string s) {
        string result;
        int balance = 0;

        for (char ch : s) {
            if (ch == '(') {
                if (balance > 0) {
                    result.push_back(ch);
                }
                balance++;
            } else { // ch == ')'
                balance--;
                if (balance > 0) {
                    result.push_back(ch);
                }
            }
        }
        return result;
    }
};

screenshot:
<img width="1859" height="837" alt="Screenshot 2026-04-10 222453" src="https://github.com/user-attachments/assets/0974d725-1ba6-41b3-8d67-74e572215b09" />

