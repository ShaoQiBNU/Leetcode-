Two Sum II - Input array is sorted
===================================

基本思路：设置两个指针，一个指向首位，一个指向末位，判断两个指针所指数字之和，如果=target，则返回；如果>target，右指针左移；如果<target，左指针右移.
-------------------------------------------------------------------------------------------------------------------------------

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
