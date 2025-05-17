# Reverse string in python(leetcode 344)

```
class Reverse:
    def reverse(self,s):
        l,r=0,len(s)-1
        while l<r:
            s[l],s[r]=s[r],s[l]
            l,r=l+1,r-1
```

#### Purpose of the Code
This Python code defines a class Reverse with a method reverse() that reverses a list (or mutable sequence) in-place (modifies the original list without returning a new one).

### Line-by-Line Explanation

1. class Reverse:
Defines a class named Reverse (follows Python naming conventions).

2. def reverse(self, s):
Defines a method reverse that takes:

self → Reference to the instance (standard in Python class methods).

s → The list/sequence to be reversed.

3. l, r = 0, len(s) - 1
Initializes two pointers:

l (left pointer) at index 0 (start of the list).

r (right pointer) at last index (len(s) - 1).

4. while l < r:
Runs a loop until the left pointer (l) crosses the right pointer (r), ensuring we only swap until the middle.

5. s[l], s[r] = s[r], s[l]
Swaps elements at positions l and r using Python’s tuple unpacking (no temporary variable needed).

6. l, r = l + 1, r - 1
Moves the left pointer forward (l += 1) and the right pointer backward (r -= 1).

#### Key Takeaways

1. In-Place Reversal: Modifies the original list (s) instead of creating a new one.

2. Two-Pointer Technique: Efficiently swaps elements from both ends towards the center.

3. Works on Mutable Sequences: Only works if s is mutable (e.g., lists). For strings (immutable), convert to a list first.

Example Usage
python
rev = Reverse()  # Create an instance
s = ['h', 'e', 'l', 'l', 'o']
rev.reverse(s)   # Reverse in-place
print(s)         # Output: ['o', 'l', 'l', 'e', 'h']
Time & Space Complexity
Time: O(n) (single pass through half the list).

Space: O(1) (no extra memory used).

## Improvement for Strings
Since strings are immutable in Python, you’d need to convert them to a list first:
```
python
s = list("hello")  # Convert to list
rev.reverse(s)     # Reverse in-place
reversed_str = ''.join(s)  # Convert back to string
print(reversed_str)  # Output: "olleh"
```
