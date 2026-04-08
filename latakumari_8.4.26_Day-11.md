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

<img width="1920" height="1020" alt="Screenshot 2026-04-08 230412" src="https://github.com/user-attachments/assets/1d41854e-6480-4d62-bd16-8d381eaa9209" />
