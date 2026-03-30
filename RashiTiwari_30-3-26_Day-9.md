Problem Statement- LINKED LIST CYCLE

Given head, the head of a linked list, determine if the linked list has a cycle in it.

There is a cycle in a linked list if there is some node in the list that can be reached again by continuously following the next pointer. Internally, pos is used to denote the index of the node that tail's next pointer is connected to. Note that pos is not passed as a parameter.

CODE: 
 class Solution {
 
       public:
        bool hasCycle(ListNode *head) {
        if (!head || !head->next) return false; 
        
        ListNode* slow = head;
        ListNode* fast = head;
        
        while (fast && fast->next) {
            slow = slow->next;          // move 1 step
            fast = fast->next->next;    // move 2 steps
            
            if (slow == fast) return true; // cycle detected
        }
        
        return false; // no cycle
    }
};

SCREENSHOT:
<img width="1886" height="838" alt="Screenshot 2026-03-30 212720" src="https://github.com/user-attachments/assets/2ef2e1f7-0037-412b-9916-be2ef6c3a05b" />

