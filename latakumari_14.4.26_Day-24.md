class Solution {
public:
    int findCenter(vector<vector<int>>& edges) {
        if (edges[0][0] == edges[1][0] || edges[0][0] == edges[1][1])
            return edges[0][0];
        return edges[0][1];
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-14 053640" src="https://github.com/user-attachments/assets/2aef5156-4c2a-47c4-9375-6dcb084d6a1f" />

