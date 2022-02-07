**Hii**
**Question link:-** https://leetcode.com/problems/find-the-difference/submissions/

◾ [Sort] sort result are the same for s and t
◾[Xor] xor value of all character is the same for s and t and XOR these two result will get zero.
**CODE**



approch 1
```
 char findTheDifference(string s, string t) {
        int n = s.length();
        sort(s.begin(), s.end());
        sort(t.begin(), t.end());
        for(int i=0; i<n; i++) if(s[i]!=t[i]) return t[i];
        return t[n];
    }
};
```

approch 2
```
class Solution {
public:
    char findTheDifference(string s, string t) {
        char ret ='\0';
        for (auto &c: s) ret^=c;
        for (auto &c: t) ret^=c;
        return ret;
    }
};
```
