class Solution {
public:
    int fib(int n) {
        if (n <= 1) return n;
        int a = 0, b = 1;
        for (int i = 2; i <= n; i++) {
            int c = a + b;
            a = b;
            b = c;
        }
        return b;
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-19 224552" src="https://github.com/user-attachments/assets/950fe276-9586-4911-971e-323b1b5cf1cb" />

