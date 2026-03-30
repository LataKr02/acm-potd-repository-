class Solution {
public:
    bool hasCycle(ListNode *head) {
        ListNode *slow = head;
        ListNode *fast = head;

        while (fast != nullptr && fast->next != nullptr) {
            slow = slow->next;          
            fast = fast->next->next;    

            if (slow == fast) {
                return true;    
            }
        }

        return false;   
    }
};


        <img width="1920" height="1080" alt="Screenshot 2026-03-30 232704" src="https://github.com/user-attachments/assets/9bfeaed5-8a91-4bbc-9d13-cb42bab77398" />
