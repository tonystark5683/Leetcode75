1768. Merge Strings Alternately
You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.

 

Example 1:

Input: word1 = "abc", word2 = "pqr"
Output: "apbqcr"
Explanation: The merged string will be merged as so:
word1:  a   b   c
word2:    p   q   r
merged: a p b q c r
Example 2:

Input: word1 = "ab", word2 = "pqrs"
Output: "apbqrs"
Explanation: Notice that as word2 is longer, "rs" is appended to the end.
word1:  a   b 
word2:    p   q   r   s
merged: a p b q   r   s

##code 
```cpp
class Solution {
public:
    string mergeAlternately(string word1, string word2) {
        int n = word1.length();
        int m = word2.length();
        string s="";
        int i=0,j=0;
        while(i< word1.length() && j<word2.length()){
            s+=word1[i];
            i++;
            s+=word2[j];
            j++;
        }
        while(i<word1.length()){
            s+=word1[i];
            i++;        
            }
        while(j<word2.length()){
            s+=word2[j];
            j++;
        }
        return s;
    }
};>
