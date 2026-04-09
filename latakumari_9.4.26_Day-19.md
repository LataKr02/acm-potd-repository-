class Solution {
public:
    bool backspaceCompare(string s, string t) {
        return process(s) == process(t);
    }
    
private:
    string process(string str) {
        string result = "";
        for (char c : str) {
            if (c == '#') {
                if (!result.empty()) {
                    result.pop_back();
                }
            } else {
                result += c;
            }
        }
        return result;


        
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-09 233058" src="https://github.com/user-attachments/assets/08ac6570-a280-424a-825f-d8fd34fc09a2" />
