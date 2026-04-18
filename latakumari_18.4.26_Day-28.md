/**
 * Definition for a binary tree node.
 * struct TreeNode {
 * int val;
 * TreeNode *left;
 * TreeNode *right;
 * TreeNode() : val(0), left(nullptr), right(nullptr) {}
 * TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 * TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
class Solution {
public:
    bool isSubtree(TreeNode* root, TreeNode* subRoot) {
        // If the main tree is empty, subRoot cannot be a subtree
        if (!root) return false;
        
        // 1. Check if the tree rooted at the current 'root' is identical to subRoot
        if (isSameTree(root, subRoot)) return true;
        
        // 2. If not, check the left and right children of 'root'
        return isSubtree(root->left, subRoot) || isSubtree(root->right, subRoot);
    }

private:
    bool isSameTree(TreeNode* s, TreeNode* t) {
        // If both nodes are null, the trees are identical at this position
        if (!s && !t) return true;
        
        // If one is null and the other isn't, or values don't match, they aren't identical
        if (!s || !t || s->val != t->val) return false;
        
        // Check both left and right children recursively
        return isSameTree(s->left, t->left) && isSameTree(s->right, t->right);
    }
};
<img width="1920" height="1020" alt="Screenshot 2026-04-18 214430" src="https://github.com/user-attachments/assets/447d0176-e8c4-4011-9240-bdf83a4d9a87" />

