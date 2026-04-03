Problem statement - Palindrome Linked List

Given the head of a singly linked list, return true if it is a palindrome or false otherwise

CODE:
class Solution {
public:
  
    bool isPalindrome(ListNode* head) {
        if (!head || !head->next) return true;

        ListNode* slow = head;
        ListNode* fast = head;
        while (fast && fast->next) {
            slow = slow->next;
            fast = fast->next->next;
        }

        ListNode* prev = nullptr;
        ListNode* curr = slow;
        while (curr) {
            ListNode* nxt = curr->next;
            curr->next = prev;
            prev = curr;
            curr = nxt;
        }
        ListNode* ptr1 = head;
        ListNode* ptr2 = prev;
        while (ptr2) {
            if (ptr1->val != ptr2->val) return false;
            ptr1 = ptr1->next;
            ptr2 = ptr2->next;
        }

Screenshot:
<img width="1823" height="824" alt="Screenshot 2026-04-04 001309" src="https://github.com/user-attachments/assets/8531bd33-4bea-422a-ab90-af677e82df94" />


        return true;
    }
};
