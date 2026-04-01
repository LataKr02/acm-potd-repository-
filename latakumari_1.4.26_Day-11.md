class Solution {
public:
    ListNode* mergeTwoLists(ListNode* list1, ListNode* list2) {
        vector <int> vals;

        while (list1) { vals.push_back(list1->val); list1 = list1->next; }
        while (list2) { vals.push_back(list2->val); list2 = list2->next; }

        sort(vals.begin(), vals.end());

        ListNode* dummy = new ListNode(0);
        ListNode* curr = dummy;
        for (int v : vals) {
            curr->next=new ListNode(v);
            curr = curr->next;
        }
        return dummy->next;
        
    }
};

<img width="1920" height="1080" alt="Screenshot 2026-04-01 223029" src="https://github.com/user-attachments/assets/f33403ed-60e9-4e0c-a9b2-e8564d264554" />
