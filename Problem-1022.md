**Hii**
**Question link:-** https://leetcode.com/problems/sum-of-root-to-leaf-binary-numbers/submissions/

◾ We are given a binary tree with all node values as 0s and 1s like 1->1->0->0 which represent the binary representation (1100).<br>
◾ Each path represent a number we have to find the sum of all these numbers


**CODE**

```
class Solution {
    private:
   int ans;
    int dfs_sum(TreeNode* root , int ans)
    {        
        if(root==NULL)   //base case
        { return 0; }
        
        ans = 2*ans + root->val;        //converting the bit into decimel while transvering to top to bottom.
        
        if(root->left == NULL && root->right == NULL)  //if this is true it represent we reach the leaf node.
        { return ans; }
       
        return dfs_sum(root->left,ans) + dfs_sum(root->right,ans);  //dfs call 
    }

public:
    int sumRootToLeaf(TreeNode* root)    //function that main will call (given in question)
    {
        return dfs_sum(root,ans);    
    }
};
```
