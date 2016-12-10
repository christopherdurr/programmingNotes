#List of algorithms and how to implement them
##By Christopher Durr

**Binary Search**

What it does: Finds an item from an ordered list of items

How: Repeatedly dividing in half the portion of the list that could contain the item, until we've narrowed down the possible locations to just one. 

Runtime: O(log n)
Here's a pseudocode description of binary search:

1. Let min = 0 and max = n-1.
2. If max < min, then stop: target is not present in array. Return -1.
3. Compute guess as the average of max and min, rounded down (so that it is an integer).
4. If array[guess] equals target, then stop. You found it! Return guess.
5. If the guess was too low, that is, array[guess] < target, then set min = guess + 1.
7. Otherwise, the guess was too high. Set max = guess - 1.
8. Go back to step 2.

