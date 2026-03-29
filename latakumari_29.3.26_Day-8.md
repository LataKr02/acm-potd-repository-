class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        ListNode* prev = nullptr;
        ListNode* curr = head;

        while (curr != nullptr) {
            ListNode* next = curr->next; 
            curr->next = prev;           
            prev = curr;                 
            curr = next;                 
        }

        return prev; 
        
    }
};
<img width="1920" height="1080" alt="Screenshot 2026-03-29 233036" src="https://github.com/user-attachments/assets/9c2b2ac1-ed53-4fee-8240-f1de038c6b50" />

