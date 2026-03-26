Day 5 – ACM POTD

🧩 Product of Array Except Self

- Description :
Given an array nums, compute a new array where each element is the product of all other elements except itself, without using division.
This solution first store the product of elements before each index, then multiply it with the product of elements after each index, achieving an O(n) time solution.
---

## Screenshot

![Result](Screenshot/IMG_20260326_213729.jpg)

---

## Code
```cpp
class Solution {
public:
    vector<int> productExceptSelf(vector<int>& nums) {
        int n = nums.size();
        vector<int> arr(n, 1);

        int left = 1;
        for (int i = 0; i < n; i++) {
            arr[i] = left;
            left *= nums[i];
        }
        int right = 1;
        for (int i = n - 1; i >= 0; i--) {
            arr[i] *= right;
            right *= nums[i];
        }
        return arr;
    }
};
```
---

 Time Complexity: O(n)
