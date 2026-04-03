class Solution {
public:
    ListNode *getIntersectionNode(ListNode *headA, ListNode *headB) {
        if (!headA || !headB) return nullptr;

        ListNode *pA = headA;
        ListNode *pB = headB;

        // When a pointer reaches the end of its list,
        // redirect it to the head of the OTHER list.
        // They will meet at the intersection node,
        // or both become nullptr if no intersection exists.
        while (pA != pB) {
            pA = (pA == nullptr) ? headB : pA->next;
            pB = (pB == nullptr) ? headA : pB->next;
        }

        return pA; // Either the intersection node or nullptr
        
    }
};

<img width="1920" height="1020" alt="Screenshot 2026-04-03 185447" src="https://github.com/user-attachments/assets/d6215e2a-9dc5-44a2-9f14-fd7df4420f01" />
