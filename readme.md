**Задача:**
**Write a function that takes the binary representation**
**Решение:**
```cpp
class Solution {
public:
    int hammingWeight(int n) {
       int count = 0;
        while (n > 0) {
            count += n & 1;
            n >>= 1;
        }
        return count; 
    }
};
```
**Задача:**
**509.The Fibonacci numbers, commonly denoted F(n) form a sequence, called the Fibonacci sequence**
**Решение:**
```cpp
class Solution {
public:
    int fib(int n) {
        if (n == 0) {
return 0;
} else if (n == 1) {
return 1;
}

int a = 0;
int b = 1;
int c;

for (int i = 2; i <= n; i++) {
c = a + b;
a = b;
b = c;
}

return c;  
    }
};
```
**Задача:**
**2455.Given an integer array nums of positive integers, return the average value of all even integers that are divisible by 3.**
**Решение:**
```cpp
class Solution {
public:
    int averageValue(vector<int>& nums) {
        int sum = 0, count = 0;
        for (int num : nums) {
            if (num % 2 == 0 && num % 3 == 0) {
                sum += num;
                count++;
            }
        }
        
        return count == 0 ? 0: sum / count;
    }
};
```