### To do : Find missing value in an arr using optimised approach in range [0,n]

#### My code:
```python
def missingNumber(self, nums):
        for i in range (len(nums)+1):
            if i not in nums:
                return i
```
#### Issues
- High time complexity
- The code goes through all the elements
---
#### Correction
- Instead of going through every number use math
- If all numbers from 0,n were present then the **Total** would be 0+1+...+n
- **For this formula is : $n * (n+1) // 2$**
- Now get the **ActualSum** since number is missing
- **Then perform $Total - ActualSum$**

#### Corrected code
```python
def missingNumber(self,nums):
        n=len(nums)
        total = n*(n+1)//2
        actualSum=0
        for i in nums:
                actualSum+=i
        
        return total-actualSum
