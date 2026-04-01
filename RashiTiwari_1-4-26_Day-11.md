Problem Statement- Merge Two Sorted Lists

You are given the heads of two sorted linked lists list1 and list2.
Merge the two lists into one sorted list. The list should be made by splicing together the nodes of the first two lists.
Return the head of the merged linked list.

Code:

 class Solution {
public:

    ListNode* mergeTwoLists(ListNode* l1, ListNode* l2) {
        ListNode temp(0);       
        ListNode* tail = &temp; 

        while (l1 && l2) {
            if (l1->val < l2->val) {
                tail->next = l1;
                l1 = l1->next;
            } else {
                tail->next = l2;
                l2 = l2->next;
            }
            tail = tail->next;
        }

        tail->next = l1 ? l1 : l2;

        return temp.next; 
    }
};


Screenshot:
<img width="1875" height="848" alt="Screenshot 2026-04-01 220833" src="https://github.com/user-attachments/assets/dd72428d-3b89-43b2-847d-bcf39a9637f8" />

