class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> seen; 

        for (int i = 0; i < nums.size(); i++) {
            int complement = target - nums[i];

            if (seen.count(complement))
                return {seen[complement], i};

            seen[nums[i]] = i;
        }
        return {};
        
    }
};
<img width="1920" height="1080" alt="Screenshot 2026-03-23 214223" src="https://github.com/user-attachments/assets/1d1e7e15-581e-45ec-b6e2-57b79dcfe4af" />


