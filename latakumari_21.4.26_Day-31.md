class Solution {
public:
    int climbStairs(int n) {
        // Base cases
        if (n <= 2) return n;
        
        int prev2 = 1; // Ways to reach step 1
        int prev1 = 2; // Ways to reach step 2
        int current = 0;
        
        for (int i = 3; i <= n; i++) {
            current = prev1 + prev2;
            // Update variables for the next step
            prev2 = prev1;
            prev1 = current;
        }
        
        return current;
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-21 201353" src="https://github.com/user-attachments/assets/e58a873f-4fa9-4b3c-9d5a-81b9f3556c72" />

