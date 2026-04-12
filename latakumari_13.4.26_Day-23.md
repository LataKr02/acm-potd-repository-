class Solution {
public:
    int findJudge(int n, vector<vector<int>>& trust) {
        vector<int> trustCount(n + 1, 0);  // How many people trust this person
        vector<int> trusts(n + 1, 0);      // How many people this person trusts
        
        for (auto& t : trust) {
            trusts[t[0]]++;     // t[0] trusts someone
            trustCount[t[1]]++; // t[1] is trusted by someone
        }
        
        for (int i = 1; i <= n; i++) {
            // Judge trusts nobody (trusts[i] == 0)
            // Everyone else trusts the judge (trustCount[i] == n - 1)
            if (trusts[i] == 0 && trustCount[i] == n - 1) {
                return i;
            }
        }
        
        return -1;
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-13 030731" src="https://github.com/user-attachments/assets/131687cb-ffa9-4570-9c55-df2609c5277d" />

