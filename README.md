# greeksquestion_1
class Solution:
    def productSelf(self, nums, n):
        res = [0] * n
      

        zero_count = 0
        product = 1
        
        arr1 = list(map(int, input().split()))
        for num in nums:
            if num != 0:
                product *= num
            else:
                zero_count += 1

        if zero_count > 1:
            return res
        if zero_count == 1:
            for i in range(n):
                if nums[i] == 0:
                    res[i] = product
            return res


        for i in range(n):
            res[i] = product // nums[i]

        return res
if __name__ == "__main__":
    sol = Solution()

    print(f"Input: {arr1}")
    print(f"Output: {sol.productSelf(arr1, len(arr1))}")

