class Solution:
    def findMaxAverage(self, nums: List[int], k: int) -> float:
        result = -float('inf')
        for i in range(len(nums) - k + 1):
            sum = 0
            for j in range(i, i + k):
                sum += nums[j]
            avg = sum/k
            if avg > result:
                result = avg
        return result
