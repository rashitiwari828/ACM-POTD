Problem Statement - Valid Parenthesis

Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

An input string is valid if:

Open brackets must be closed by the same type of brackets.
Open brackets must be closed in the correct order.
Every close bracket has a corresponding open bracket of the same type.

code:
class Solution {
public:

bool isValid(string s) {

    stack<char> st;
    
    for(char c : s) {
        if(c == '(' || c == '{' || c == '[') {
        
            st.push(c);
        } else {
            if(st.empty()) return false;
            char top = st.top();
            st.pop();
            if((c == ')' && top != '(') ||
           (c == '}' && top != '{') ||
               (c == ']' && top != '[')) {
                return false;
            }
        }
    }
    return st.empty();
}
};


Screenshot:<img width="1862" height="855" alt="Screenshot 2026-04-05 210847" src="https://github.com/user-attachments/assets/40252820-cfd9-401d-9327-044cb2a6aa92" />



    
};
