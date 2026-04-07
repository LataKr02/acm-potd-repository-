class Solution {
public:
    vector<int> nextGreaterElement(vector<int>& nums1, vector<int>& nums2) {
        
        unordered_map<int, int> nge;
        
        stack<int> st;

        for (int num : nums2) {
            
            while (!st.empty() && st.top() < num) {
                nge[st.top()] = num;
                st.pop();
            }
            st.push(num);
        }

        
        while (!st.empty()) {
            nge[st.top()] = -1;
            st.pop();
        }
        
        vector<int> ans;
        for (int num : nums1) {
            ans.push_back(nge[num]);
        }
        return ans;
        
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-07 225125" src="https://github.com/user-attachments/assets/eb693410-dc42-4c80-8a19-a784ab61a240" />

