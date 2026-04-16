problem statement - Invert Binary Tree

code:
class Solution {
public:

    TreeNode* invertTree(TreeNode* root) {
      if (root == nullptr) return nullptr;
        TreeNode* temp = root->left;
        root->left = root->right;
        root->right = temp;
        invertTree(root->left);
        invertTree(root->right);
        return root;
    }
};

Screenshot:
<img width="1715" height="791" alt="image" src="https://github.com/user-attachments/assets/9c569ddf-9eac-459f-8c64-b525718b88c5" />
