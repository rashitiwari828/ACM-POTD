Problem Statement - Make the string great

code:
class Solution {
public:

    string makeGood(string s) {
          string st;
    for (char c : s) {
        if (!st.empty() && abs(st.back() - c) == 32) {
            st.pop_back();
        } else {
            st.push_back(c);
        }
    }
    return st;
    }
};

Screenshot:
<img width="1878" height="799" alt="Screenshot 2026-04-11 221043" src="https://github.com/user-attachments/assets/afb80eed-adc0-4ac3-9e80-16f5681326c8" />
