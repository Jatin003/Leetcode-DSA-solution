**Hyy so i have two approches to solve this one:-**
**Question Link:-** https://leetcode.com/problems/add-binary/
1. Long one in which u first convert the a and b to decimal add them and convert back
2. An optimize in which u do binary add and store it in "ans" string and return it rather then converting the whole binary string into decimal.

<br>

So where is the second one explained with comments :D.

```
class Solution {
public:
    string addBinary(string a, string b) {
        int i = a.size()-1;  //i and j while be used to acces the srting by index 
        int j = b.size()-1;
        int c=0;     // while be used to keep track of the carry
        string ans=""; //result will be stored in this string
        while(i>=0|| j>=0){
                    
                    //loop till both index becomes 0 and add last bit of both the string along with carry keep track of carry .
    
            int x = (i>=0)?a[i--]-'0' : 0 ; 
            int y = (j>=0)?b[j--]-'0' : 0 ;
    
            int sum = x+y+c;
            
            ans=to_string(sum%2)+ans; //reminder by two is the new ans bit
            c=sum/2;  //it keep tracks of carry
        }
    
        if(c>0)
        {
               ans=to_string(1)+ans;
        }
        return ans;     
    }
};
```
