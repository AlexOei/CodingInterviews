# Coding Interviews
[Sliding Window](https://github.com/AlexOei/CodingInterviews/blob/main/README.md#sliding-window)


## Sliding Window

### Clarifying Questions:
- Time and Space Constraints
- Inputs
  - Can the inputs be empty?
  - Will the inputs be valid?
  - Can the inputs be negative?
- Solutions
  - What do I return if there is no solution?
  - What do I return if there are multiple solutions?

### General Psuedocode:  
```
class Solution:
    def something(self, s: str, t: str) -> str:
    
        Prereq Variables: left and/or right pointer, current result, best result
        Prereq Structures: usually hashmap, array, or dequeue
        Process Inputs if needed

        Base Cases: If null or constraint is not fulfilled
        
        Iterate through Array
            Add to window if constraint is fulfilled
            Check if answer is better if constraint is fulfilled
            Move left pointer if constraint is fulfilled
        Return answer
        
```



#### Best Time to Buy and Sell Stock Easy

Brute Force:
  try every combination starting at each number in the array. Time complexity of n^2

Optimized Algorithm: 
- Structures: buy = 0, currentProfit, maxProfit
- Base Case: if list is less than length 2, return 0, as there you can't sell
- Start at the first day you can sell, day 2
  - determine the profit
  - if greater than current profit, store the value
  - if the value is less than the day we buy, move the buy pointer
- Return the maxProfit if > 0, otherwise return 0

```
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        buy = 0
        curProfit = float('-infinity')
        maxProfit = float('-infinity')
        
        for day in range(1, len(prices)):
            curProfit = prices[day] - prices[buy]
            maxProfit = max(curProfit, maxProfit)
            if prices[day] < prices[buy]:
                buy = day
                
        if maxProfit > 0:
            return maxProfit
        return 0

```


#### Longest Substring Without Repeating Characters Medium

#### Longest Repeating Character Replacement Medium

#### Permutation in String Medium

#### Minimum Window Substring

#### Sliding Window Maximum

## Two Pointers

## Fast and Slow Pointers

## Merge Intervals

## Cyclic Sort

## Linked List Reversal

## BFS

## DFS

## Heaps

## Subsets

## Binary Search

## K elements

## K Merge

## Dynamic Programming

## Topological Sort


