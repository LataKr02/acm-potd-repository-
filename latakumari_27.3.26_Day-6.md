class Solution {
public:
    bool checkSubarraySum(vector<int>& nums, int k) {
        unordered_map<int, int> remainderIndex;
        remainderIndex[0] = -1;
        int prefixSum = 0;

        for (int i = 0; i < nums.size(); i++) {
            prefixSum += nums[i];
            int remainder = prefixSum % k;

            if (remainderIndex.count(remainder))  {
                if (i - remainderIndex[remainder] >=2) {
                return true;
            }
        } else {
            remainderIndex[remainder] = i;
        }
    }
<img width="1920" height="1080" alt="Screenshot 2026-03-27 202235" src="https://github.com/user-attachments/assets/7b7c1dcc-6ffd-43f7-a5bb-16a28f91adb5" />

    return false;

    
