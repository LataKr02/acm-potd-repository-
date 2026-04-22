class Solution {
public:
    int lengthOfLIS(vector<int>& nums) {
        vector<int> tails; // tails[i] = smallest tail element of all IS of length i+1

        for (int num : nums) {
            // Binary search for first element in tails >= num
            auto it = lower_bound(tails.begin(), tails.end(), num);

            if (it == tails.end())
                tails.push_back(num);   // num extends the longest subsequence
            else
                *it = num;              // Replace to keep tail as small as possible
        }

        return tails.size();
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-22 210446" src="https://github.com/user-attachments/assets/edbc69ea-8787-45ac-92bf-d6e343aab6e0" />

