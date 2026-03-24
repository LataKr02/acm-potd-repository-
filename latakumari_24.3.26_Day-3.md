class Solution {
public:
    void sortColors(vector<int>& nums) {
        int low = 0, mid = 0, high = nums.size() - 1;

        while (mid <= high) {
            if (nums[mid] == 0) {
                swap(nums[low], nums[mid]);
                low++;
                mid++;
            } else if (nums[mid] == 1) {
                mid++;
            } else { 
                swap(nums[mid], nums[high]);
                high--;
                
            }
        }<img width="1920" height="1080" alt="Screenshot 2026-03-24 230636" src="https://github.com/user-attachments/assets/f0f68e99-3440-4638-9f35-4f23842fe920" />

        
    }
};
