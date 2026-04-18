Problem Statement -  Subtree of Another Tree

code:
class Solution {
public:

    bool isSubtree(TreeNode* root, TreeNode* subRoot) {
        if (!root) return false;
        if (isSame(root, subRoot)) return true;
        return isSubtree(root->left, subRoot) || isSubtree(root->right, subRoot);
    }

    bool isSame(TreeNode* s, TreeNode* t) {
        if (!s && !t) return true;
        if (!s || !t) return false;
        if (s->val != t->val) return false;
        return isSame(s->left, t->left) && isSame(s->right, t->right);
    } 
    
};

screenshot:
<img width="1754" height="728" alt="Screenshot 2026-04-19 001759" src="https://github.com/user-attachments/assets/87b70853-c33e-4b33-9f79-649d88357a05" />
