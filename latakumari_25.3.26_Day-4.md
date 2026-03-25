class Solution {
public:
    vector<int> twoSum(vector<int>& numbers, int target) {
        int left = 0, right = numbers.size() - 1;
        
        while (left < right) {
            int sum = numbers[left] + numbers[right];
            
            if (sum == target) {
                return {left + 1, right + 1};  
            } else if (sum < target) {
                left++;   
            } else {
                right--; 
            }
        }
        
        return {};  
        
    }
};

<img width="1920" height="1080" alt="Screenshot 2026-03-25 230448" src="https://github.com/user-attachments/assets/79e7a7f9-fae7-494a-a52f-60213fbd4b78" />
