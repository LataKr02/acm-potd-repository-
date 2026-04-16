class Solution {
public:
    TreeNode* invertTree(TreeNode* root) {
        if (!root) return nullptr;
        
        swap(root->left, root->right);
        
        invertTree(root->left);
        invertTree(root->right);
        
        return root;
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-16 231505" src="https://github.com/user-attachments/assets/65d9a6c9-f6e1-4b37-ba31-be692b763294" />

