Day 4 – ACM POTD

🧩 Missing Number

- Description :
Given an array containing n distinct numbers in the range [0, n], find the one number that is missing from the array.
This solution uses the XOR approach, which efficiently finds the missing number by cancelling out common elements.
---

## Screenshot

![Result](Screenshot/IMG_20260323_232120.jpg)

---

## Code
```cpp
class Solution {
public:
    int missingNumber(vector<int>& nums) {
        int n = nums.size();
        int a = 0, b = 0;

        for (int i = 0; i <= n; i++) {
            a ^= i;
        }

        for (int i = 0; i < n; i++) {
            b ^= nums[i];
        }

        return a ^ b;
    }
};
```
---

 Time Complexity: O(n)
