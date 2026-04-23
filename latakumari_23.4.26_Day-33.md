#include <vector>
#include <numeric>

using namespace std;

class Solution {
public:
    bool canPartition(vector<int>& nums) {
        int sum = 0;
        for (int num : nums) {
            sum += num;
        }
        
        // If the total sum is odd, it cannot be partitioned into two equal subsets
        if (sum % 2 != 0) {
            return false;
        }
        
        int target = sum / 2;
        
        // dp[i] will be true if a subset with sum i is possible
        vector<bool> dp(target + 1, false);
        dp[0] = true; // A sum of 0 is always possible with an empty subset
        
        for (int num : nums) {
            // Traverse backwards to avoid using the same element multiple times
            for (int j = target; j >= num; --j) {
                dp[j] = dp[j] || dp[j - num];
            }
        }
        
        return dp[target];
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-23 223813" src="https://github.com/user-attachments/assets/b45702e0-8587-45bd-8df2-13bbd72526a8" />

