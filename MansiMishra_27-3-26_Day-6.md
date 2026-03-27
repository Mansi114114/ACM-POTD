Day 6 – ACM POTD

🧩 Check if N and its Double Exist

- Description :
Given an array, check if any two different elements exist such that one is double the other. The solution uses two nested loops to compare all pairs and returns true if arr[i] == 2 * arr[j]; otherwise, it returns false.
---

## Screenshot

![Result](Screenshot/IMG_20260327_130652.jpg)

---

## Code
```cpp
class Solution {
public:
    bool checkIfExist(vector<int>& arr) {
        int size =arr.size();
        for (int i=0;i<size ;i++){
            for (int j=0;j<size ;j++){
                if (i != j && arr[i]== 2*arr[j]){
                    return true;
                }
            }
        }
        return false;
    }
};
```
---

 Time Complexity: O(n²)
