class Solution {
public:
    bool increasingTriplet(vector<int>& nums) {
        int first = INT_MAX, second = INT_MAX;
        
        for (int n : nums) {
            if (n <= first) {
                first = n;          
            } else if (n <= second) {
                second = n;         
            } else {
                return true;        
            }
        }
        
        return false;
        
    }
};

<img width="1920" height="1080" alt="Screenshot 2026-03-28 222840" src="https://github.com/user-attachments/assets/65da43c8-e84c-4278-9f24-78ce9e861e60" />
