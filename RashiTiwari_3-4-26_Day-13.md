Problem Statement- Intersection of two linked lists

code:

class Solution {
public:
  ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {

        if (!headA || !headB) return nullptr;
        
        ListNode* ptrA = headA;
        ListNode* ptrB = headB;
        
        while (ptrA != ptrB) {
            ptrA = (ptrA == nullptr) ? headB : ptrA->next;
            ptrB = (ptrB == nullptr) ? headA : ptrB->next;
        }
          return ptrA; // either intersection node or nullptr
    }
};

screenshot:
<img width="1872" height="837" alt="Screenshot 2026-04-04 000631" src="https://github.com/user-attachments/assets/859e6026-780a-4821-aea8-b9f32493006b" />
