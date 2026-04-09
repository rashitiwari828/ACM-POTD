Problem Statement- Backspace string compare

Given two strings s and t, return true if they are equal when both are typed into empty text editors. '#' means a backspace character.

Note that after backspacing an empty text, the text will continue empty

code:
class Solution {
public:

    bool backspaceCompare(string s, string t) {
            return build(s) == build(t);
    }
    private:
    string build(string str) {
        string result;
        for (char c : str) {
            if (c != '#') {
                result.push_back(c);
            } else if (!result.empty()) {
                result.pop_back();
            }
        }
        return result;
    }
};

screenshot:
<img width="1784" height="837" alt="Screenshot 2026-04-09 224604" src="https://github.com/user-attachments/assets/54e5b599-dfb2-4b3f-abc6-b85d76ee04ef" />




    
