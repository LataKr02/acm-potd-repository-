class Solution {
public:
    ListNode* deleteDuplicates(ListNode* head) {
        ListNode* current = head;

        while (current != nullptr && current->next != nullptr) {
            if (current->val == current->next->val)  {

                ListNode* duplicate = current->next;
                current->next = current->next->next;
                delete duplicate;
            } else {

                current = current->next;
            }
        }
        return head;
        
    }
};

<img width="1920" height="1020" alt="Screenshot 2026-04-02 222025" src="https://github.com/user-attachments/assets/2108cf21-1d5f-4e9a-ae90-7f66e1477f7e" />
