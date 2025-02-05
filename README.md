[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/6wGdpkN5)
# Longest Nice Substring
```
class Solution {
public:
    string longestNiceSubstring(string s) {
        if (s.size() < 2) return "";

        unordered_set<char> charSet(s.begin(), s.end());

        for (int i = 0; i < s.size(); i++) {
            if (charSet.count(tolower(s[i])) && charSet.count(toupper(s[i]))) continue;
            
            // Recursively check left and right substrings
            string left = longestNiceSubstring(s.substr(0, i));
            string right = longestNiceSubstring(s.substr(i + 1));

            return left.size() >= right.size() ? left : right;
        }
        
        return s; 
    }
};
```
# Output
![image](https://github.com/user-attachments/assets/001b6d9a-5053-4b9a-9b8e-8425a0bfb348)

# Reverse Bits
```
class Solution {
public:
    uint32_t reverseBits(uint32_t n) {
        uint32_t res = 0;
        
        for (int i = 0; i < 32; i++) {
            res = (res << 1) | (n & 1); 
            n >>= 1; 
        }
        
        return res;
    }
};

```
# Output
![image](https://github.com/user-attachments/assets/c696b7d4-0872-4c70-b105-15ad32d1d6c0)

# Number of 1 Bits
```
class Solution {
public:
    int hammingWeight(int n) {
        int count = 0;
        while (n) {
            n &= (n - 1); 
            count++;
        }
        return count;
    }
};

```
# Output
![image](https://github.com/user-attachments/assets/83c033f6-4582-4f32-9f23-e287f489ea79)

# Max SubArray
```

```
# Output


# Search 2d Matrix 2
```

```
# Output

# Sub Pow
```

```
# Output
























