Problem Statement- Middle of the linked list

Given the head of a singly linked list, return the middle node of the linked list.
If there are two middle nodes, return the second middle node

CODE:
class Solution {
public:

    ListNode* middleNode(ListNode* head) {
        ListNode* slow = head;
        ListNode* fast = head;
         while (fast != nullptr && fast->next != nullptr) {
            slow = slow->next;          
            fast = fast->next->next;    
        }
        
        return slow; 
    
    }
};

SCREENSHOT:
<img width="1898" height="827" alt="Screenshot 2026-03-31 210258" src="https://github.com/user-attachments/assets/d7591b74-89e0-4a6c-8622-6fc7f49920e7" />
