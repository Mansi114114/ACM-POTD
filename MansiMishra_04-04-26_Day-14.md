Day 14 – ACM POTD

🧩 Palindrome linked list

- Description :
Store values in array and use two pointers to check palindrome.

---

## Screenshot

![Result](Screenshot/IMG_20260404_225341.jpg)

---

## Code
```cpp
class Solution {
public:
    bool isPalindrome(ListNode* head) {
        vector<int> arr;

        while (head) {
            arr.push_back(head->val);
            head = head->next;
        }

        int i = 0, j = arr.size() - 1;
        while (i < j) {
            if (arr[i] != arr[j])
                return false;
            i++;
            j--;
        }

        return true;
    }
};
```
