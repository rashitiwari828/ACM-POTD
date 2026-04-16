problem statement - Maximum Depth of Binary Tree

code:class Solution {
public:

    int maxDepth(TreeNode* root) {
          if (root == nullptr) return 0;
        int leftDepth = maxDepth(root->left);
        int rightDepth = maxDepth(root->right);
        return 1 + std::max(leftDepth, rightDepth);
    }
};


screenshot:
<img width="1778" height="718" alt="Screenshot 2026-04-16 215240" src="https://github.com/user-attachments/assets/5cabefed-5998-4411-8497-d1c9cd416680" />

 
