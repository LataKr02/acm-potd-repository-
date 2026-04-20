class Solution {
public:
    bool isPowerOfTwo(int n) {
        // A power of two must be greater than 0.
        // The bitwise trick (n & (n - 1)) removes the lowest set bit.
        // If the result is 0, there was only one bit set.
        return n > 0 && (n & (long long)n - 1) == 0;
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-20 231425" src="https://github.com/user-attachments/assets/e0c17b5f-9618-4a9a-860b-fb96e877ee87" />

