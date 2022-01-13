**Hii**<br>
**Question link:-** https://leetcode.com/problems/insert-into-a-binary-search-tree/<br>
**Approch**

**step-1** so when ever a question when i have to check for common elments in containers i always Sort them first, So sort the segements by the end.
**step2** Put an arrow at the end of the 1-st array.
**Step3** Now form the second one we check whether the current arrow pass through the current segment, if not add an arrow and so on so forth.


**CODE**

```
bool cmp(vector<int>& a, vector<int>& b) {return a[1] < b[1];}
class Solution {
public:  

    int findMinArrowShots(vector<vector<int>>& segments) {
        sort(segments.begin(), segments.end(), cmp);              //step1
        int ans = 0, arrow = 0;
        
        for (int i = 0; i < segments.size(); i ++) 
        {
             if (ans == 0 || segments[i][0] > arrow)                               //ans==0 for step2 and 2nd condition for step3
             {
                ans ++;
                arrow = segments[i][1];
            }
        }
        return ans;
    }
};
```
