Day 7 – ACM POTD

🧩 Increasing Triplet Subsequence

- Description :
Given an array, check if any two different elements exist such that one is double the other. The solution uses two nested loops to compare all pairs and returns true if arr[i] == 2 * arr[j]; otherwise, it returns false.
---

## Screenshot

![Result](Screenshot/IMG_20260328_212028.jpg)

---

## Code
```cpp
class Solution {
public:
    bool increasingTriplet(vector<int>& nums) {
        int first = INT_MAX, second = INT_MAX;
        for (int num : nums) {
            if (num <= first) {
                first = num;
            } else if (num <= second) {
                second = num;
            } else {
                return true;
            }
        }
        return false;
    }
};
```
---

 Time Complexity: O(n)
