problem statement-  Remove All Adjacent Duplicates In String

code:
class Solution {
public:

    string removeDuplicates(string s) {
         string stack;
        for (char c : s) {
            if (!stack.empty() && stack.back() == c) {
                stack.pop_back(); 
            } else {
                stack.push_back(c);
            }
        }
        return stack;
    }
};

screenshot:
<img width="1794" height="817" alt="Screenshot 2026-04-08 221740" src="https://github.com/user-attachments/assets/ac5a677e-d3d9-4b92-831e-1fcbbea9333f" />
