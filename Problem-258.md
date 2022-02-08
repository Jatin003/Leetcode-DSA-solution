**Hii**<br>
**Question link:-** https://leetcode.com/problems/add-digits/

◾ Recursive Approch
◾Now this is nice one any number where it's digits add to 9 is always divisible by 9. (18, 27, 36, 45, 54, 63, 72, 81, 90, etc.)<br> Therefore the 'digital root' for any number divisible by 9 is always 9<br>
Additionally, 0 always has a digital root of 0 obviously.<br>
So for any number that isn't 0 and isn't divisible by 9, the root will always n % 9 for a given number n.<br>
For examples: 
102 % 9 = 3.

**CODE**

Approch 1
```
class Solution {
public:
    int addDigits(int num) {
      int sum=0;
        while(num)
        {
            sum+=(num%10);
            num/=10;
        }
        if(sum<10)
            return sum;
        else
            return addDigits(sum);
    }
};
```

Approch 2
```class Solution {
public:
    int addDigits(int num) {
        
        if(num==0)
        {
            return 0;
        }
        else if(num%9==0)
        {
            return 9;
        }
        else
        {
            return num%9;
        }
    }
};
```
