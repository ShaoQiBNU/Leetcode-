Two Sum II - Input array is sorted
===================================

###  
        class Solution:
                def twoSum(self, numbers, target):
                    """
                    :type numbers: List[int]
                    :type target: int
                    :rtype: List[int]
                    """
                    index=[]
                    i=0
                    j=len(numbers)-1
        
                    while True:
                        if numbers[i]+numbers[j]==target:
                            index.append(i+1)
                            index.append(j+1)
                            return index
                            break
                        elif numbers[i]+numbers[j]>target:
                            j=j-1
                        else:
                            i=i+1
