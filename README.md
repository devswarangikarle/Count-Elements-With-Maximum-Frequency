# Count-Elements-With-Maximum-Frequency
You are given an array nums consisting of positive integers.  Return the total frequencies of elements in nums such that those elements all have the maximum frequency.  The frequency of an element is the number of occurrences of that element in the array.

class Solution:
    def maxFrequencyElements(self, nums: List[int]) -> int:
        freq=[0]*101
        maxF=0
        for x in nums:
            freq[x]+=1
            maxF=max(maxF, freq[x])
        ans=0
        for f in freq:
            if f==maxF:
                ans+=f
        return ans
