class Solution {
public:
    bool isValid(string s) {
        stack<char> st;
        
        for (char c : s) {
            if (c == '(' || c == '{' || c == '[') {
                st.push(c);
            } else {
                if (st.empty()) return false;
                
                char top = st.top();
                st.pop();
                
                if (c == ')' && top != '(') return false;
                if (c == '}' && top != '{') return false;
                if (c == ']' && top != '[') return false;
            }
        }
        
        return st.empty();
        
    }
};

<img width="1920" height="1020" alt="Screenshot 2026-04-05 231625" src="https://github.com/user-attachments/assets/edd3142c-75e5-4abf-99e3-a3b7877f6415" />
