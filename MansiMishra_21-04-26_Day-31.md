Day 31 – ACM POTD

🧩 Climbing Stairs

- Description :
Uses Fibonacci pattern.
---

## Screenshot

![Result](Screenshot/Screenshot2026-04-21.png)

---

## Code
```cpp
  class Solution {
public:
    int climbStairs(int n) {
        if(n <= 2){
            return n;
        }       
        int a = 1, b = 2, c;       
        for(int i = 3; i <= n; i++) {
            c = a + b;
            a = b;
            b = c;
        }    
        return b;
    }
};
```
