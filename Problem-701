**Hii**<br>
**Question link:-** https://leetcode.com/problems/insert-into-a-binary-search-tree/<br>

◾ This is a basic insertion in BST<br>

**step-1** If the root is empty, the new tree node can be returned as the root node position found.<br>

**step2** Otherwise compare root:<br>
**1.** If root.val is greater than the target value, that means node should be inserted into the left subtree<br>
**2.** If root.val is less than the target value, that means node should be inserted into the right subtree<br>

**CODE**

```
class Solution {
public:
    TreeNode* insertIntoBST(TreeNode* root, int val) {
        
        if(!root) {return new TreeNode(val);}   //step-1
        
        if(root->val>val)
        { root->left = insertIntoBST(root->left, val);} //step-2-1
        else
        { root->right = insertIntoBST( root->right, val);}//step-2-2
        
        return root;
    }
};
```
