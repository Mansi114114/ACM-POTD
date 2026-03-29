Day 8 – ACM POTD

🧩 Increasing Triplet Subsequence

- Description :
The solution checks if there exists an increasing triplet in the array. It uses two arrays to store the minimum value on the left and maximum value on the right for each element. If any element has a smaller value before it and a greater value after it, a triplet exists.
---

## Screenshot

![Result](Screenshot/IMG_20260329_191007.jpg)

---

## Code
```cpp
class Solution {
public:
    bool increasingTriplet(vector<int>& nums) {
        int n = nums.size();
        if (n < 3){
            return false;}

        vector<int> LMin(n), RMax(n);

        LMin[0] = nums[0];
        for (int i = 1; i < n; i++) {
            LMin[i] = min(LMin[i-1], nums[i]);
        }

        RMax[n-1] = nums[n-1];
        for (int i = n-2; i >= 0; i--) {
            RMax[i] = max(RMax[i+1], nums[i]);
        }

        for (int i = 1; i < n-1; i++) {
            if (LMin[i-1] < nums[i] && nums[i] < RMax[i+1]) {
                return true;
            }
        }
        return false;
    }
};
```
---

 Time Complexity: O(n)
