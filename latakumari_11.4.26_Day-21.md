class Solution {
public:
    string makeGood(string s) {
        string stack;
        for (char c : s) {
            if (!stack.empty() && abs(stack.back() - c) == 32) {
                stack.pop_back();
            } else {
                stack.push_back(c);
            }
        }
        return stack;
        
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-11 220510" src="https://github.com/user-attachments/assets/56c7dcf4-9847-4065-b406-383d221e9e0d" />

