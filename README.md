# DSA-Repo

# 1. Majority Element
Given an array nums of size n, return the majority element.

The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.

Example 1:

Input: nums = [3,2,3]
Output: 3

Example 2:

Input: nums = [2,2,1,1,1,2,2]
Output: 2
 
Constraints:

n == nums.length
1 <= n <= 5 * 104
-109 <= nums[i] <= 109
 
Follow-up: Could you solve the problem in linear time and in O(1) space?

# Answer Using Python


 class Solution:

    def majorityElement(self, nums: List[int]) -> int:
    
        count = {}
        
        n = len(nums)
        for num in nums:
            if num not in count:
                count[num] = 0
            count[num] += 1
            if count[num] > n // 2:
                return num

# Expline

Class Definition:


# class Solution:
This line defines a class named Solution. Classes are used to encapsulate related functions and data together. In this case, it's likely designed to solve a specific problem or set of problems.
Method Definition:


# def majorityElement(self, nums: List[int]) -> int:

This line defines a method named majorityElement within the Solution class.
It takes two arguments:
self: A reference to the instance of the class. This is a standard convention in Python classes.
nums: A list of integers. This is the input list for which we need to find the majority element.
It specifies that the method returns an integer, which is the majority element.
Initialization:


# count = {}
This line initializes an empty dictionary named count. This dictionary will be used to store the count of occurrences for each unique number in the nums list.
Length Calculation:


# n = len(nums)
This line calculates the length of the nums list and assigns it to the variable n. This length will be used later in the code.
Iteration over List:


# for num in nums:
This line starts a loop that iterates over each element (num) in the nums list. It will go through each number in the list to perform counting and checking.
Counting Occurrences:


# (if num not in count:
#    count[num] = 0
# count[num] += 1)
These lines count the occurrences of each number in the nums list.
If num is not already a key in the count dictionary, it adds it with an initial count of 0.
Then it increments the count for that number by 1.
Checking Majority Condition:


# if count[num] > n // 2:
#    return num
This line checks if the count of the current num is greater than half the length of the nums list.
If it is, it means that num occurs more than n/2 times in the list, making it the majority element.
In that case, the method returns num.
        
