**Hii**
**Question link:-** https://leetcode.com/problems/sum-of-root-to-leaf-binary-numbers/submissions/

◾ We are given a binary tree with all node values as 0s and 1s like 1->1->0->0 which represent the binary representation (1100).<br>
◾ Each path represent a number we have to find the sum of all these numbers


**CODE**

```
class Solution {
    public:
   
    int sumRootToLeaf(TreeNode* root , int ans=0)
    {
        if(root==NULL)   //base case
        { return 0; }
        
        ans = 2*ans + root->val;        //as shown above this will convert the binary into decimal
        
        if(root->left == NULL && root->right == NULL)  //if this is true it represent we reach the leaf node.
        { return ans; }
       
        return  sumRootToLeaf(root->left,ans) + sumRootToLeaf(root->right,ans);  //dfs call
    }  
};
```
