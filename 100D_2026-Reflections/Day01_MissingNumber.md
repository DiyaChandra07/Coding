#To do : Find missing value in an arr using optimised approach in range [0,n]

My code:
def missingNumber(self, nums):
        for i in range (len(nums)+1):
            if i not in nums:
                return i

#issues