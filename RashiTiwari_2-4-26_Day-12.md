Problem Statement- Remove Duplicates From Sorted Lists

Given the head of a sorted linked list, delete all duplicates such that each element appears only once. Return the linked list sorted as well.

Code:
        class Solution {
public:

    ListNode* deleteDuplicates(ListNode* head) {
        if (!head) return nullptr;

        ListNode* current = head;
        while (current->next) {
            if (current->val == current->next->val) {
                // Skip the duplicate node
                current->next = current->next->next;
            } else {
                current = current->next;
            }
        }
        return head;

    }
};

Screenshot:
<img width="1874" height="852" alt="Screenshot 2026-04-02 221200" src="https://github.com/user-attachments/assets/5a3c848c-447a-4964-9c3f-751a91774746" />
