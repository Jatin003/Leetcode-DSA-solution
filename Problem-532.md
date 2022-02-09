**Hii** <br>
**Question link:-** https://leetcode.com/problems/k-diff-pairs-in-an-array/


**CODE**

```class Solution {
public:
    int findPairs(vector<int>& nums, int k) {
        
        int ans=0;
        unordered_map<int,int> map ;
        
        for(int i=0 ; i<nums.size() ; i++)
        {
            int x = nums[i];
            map[x]++;
        }
        
        for(auto a:map)
        {
            if(k==0)
            {
                if(a.second>1)
                { ans++;}
            }
            else if(map.find(a.first+k) != map.end())
                {ans++;}
        }
        return ans;      
    }
};
```
