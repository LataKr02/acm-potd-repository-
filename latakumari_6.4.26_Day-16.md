class Solution {
public:
    vector<int> dailyTemperatures(vector<int>& temperatures) {
        int n = temperatures.size();
        // Initialize the answer array with 0s. 
        // If a warmer day is never found, the value will correctly remain 0.
        vector<int> answer(n, 0); 
        
        // The stack will store the *indices* of the temperatures, not the temperatures themselves.
        stack<int> st; 

        for (int i = 0; i < n; ++i) {
            // While the stack is not empty AND the current temperature is warmer 
            // than the temperature at the index stored at the top of the stack:
            while (!st.empty() && temperatures[i] > temperatures[st.top()]) {
                int prevIndex = st.top();
                st.pop();
                // The number of days is the difference between the current index and the previous index
                answer[prevIndex] = i - prevIndex; 
            }
            // Push the current day's index onto the stack to wait for a warmer day
            st.push(i);
        }
        return answer;
        
    }
};<img width="1920" height="1020" alt="Screenshot 2026-04-06 234227" src="https://github.com/user-attachments/assets/cbac6654-bd46-4ecc-9439-446a20b410e1" />

