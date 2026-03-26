class Solution {
public:
    void moveZeroes(vector<int>& nums) {
        int left = 0; 
        
        
        for (int right = 0; right < nums.size(); right++) {
            if (nums[right] != 0) {
                nums[left] = nums[right];
                left++;
            }
        }
        
        
        while (left < nums.size()) {
            nums[left] = 0;
            left++;
        }
        
    }
};
<img width="1920" height="1080" alt="Screenshot 2026-03-26 191935" src="https://github.com/user-attachments/assets/b1fcfae1-4bc8-4677-9b66-d68cc45b0183" />
