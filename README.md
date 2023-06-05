# DSA-Assignment1

###
Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Note that you must do this in-place without making a copy of the array.

Example 1:
Input: nums = [0,1,0,3,12]
Output: [1,3,12,0,0]
###
Ans: A = [0,1,0,3,12]
n = len(A)
j = 0
for i in range(n):
    if A[i] != 0:
        A[j], A[i] = A[i], A[j]  # Partitioning the array
        j += 1
print(A)

----First Unique Character in a String ---

Given a string s, find the first non-repeating character in it and return its index. If it does not exist, return -1.

Example 1:
Input: s = "leetcode"
Output: 0

Ans:
def firstUniqChar(self, s):
    hset = collections.Counter(s);
        # Traverse the string from the beginning...
    for idx in range(len(s)):
            # If the count is equal to 1, it is the first distinct character in the list.
        if hset[s[idx]] == 1:
            return idx
    return -1 
