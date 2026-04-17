class Solution {
public:
    int diameterOfBinaryTree(TreeNode* root) {
        int diameter = 0;
        depth(root, diameter);
        return diameter;
    }

private:
    int depth(TreeNode* node, int& diameter) {
        if (!node) return 0;
        int left  = depth(node->left, diameter);
        int right = depth(node->right, diameter);
        diameter  = max(diameter, left + right);
        return 1 + max(left, right);
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-17 235216" src="https://github.com/user-attachments/assets/46eafbfc-264a-4f7e-ac67-3f637c695c14" />

