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

<img width="1920" height="1080" alt="Screenshot 2026-03-31 221507" src="https://github.com/user-attachments/assets/a6d6d86e-5edc-4add-9c7f-8819ecb1e0ff" />
