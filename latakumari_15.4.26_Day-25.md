class Solution {
public:
    int maxDepth(TreeNode* root) {
        if (root == nullptr) return 0;
        return 1 + max(maxDepth(root->left), maxDepth(root->right));
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-15 045045" src="https://github.com/user-attachments/assets/59550c02-3737-418b-83d9-cf5009b5a275" />
