**Hii**
**Question link:-** https://leetcode.com/problems/linked-list-cycle-ii/submissions/

◾Lets call this one the Rabbit and tortoise approch :D

**CODE**

```
class Solution {
public:
    ListNode *detectCycle(ListNode *head) {
        if(!head) return NULL;
        
        ListNode *slow=head,*fast=head;
        
  
        do{
            slow = slow->next;
            if(!slow) break;          
            fast= fast->next;
            if(!fast) break;
            fast = fast->next;
            if(!fast) break;            
        }while(slow!=fast);
  
        if(!slow or !fast)
            return NULL;
        
          fast = head;
        while(fast !=slow)
            fast=fast->next, slow=slow->next;
        return fast;
    }
};
```
