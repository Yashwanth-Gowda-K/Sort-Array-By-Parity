# Sort-Array-By-Parity


Problem Statement
Given an integer array, rearrange the elements so all even numbers appear before odd numbers. The order within even or odd groups does not matter.

Examples:
Input: [3, 1, 2, 4] → Output: [2, 4, 3, 1] (or any valid permutation)
Input: [0] → Output: [0]
Solution Approaches
1. Two-Pointer Technique (Optimal)
Key Idea:
Use two pointers starting at the beginning (left) and end (right) of the array.
Swap when left points to an odd number and right points to an even number.
Move pointers inward until they cross, ensuring evens end up on the left.

Performance:
⏱️ Time: O(n) (single pass)
💾 Space: O(1) (in-place modification)

Edge Cases Handled:
Arrays with all even/odd numbers
Single-element arrays
2. Partition-Based Approach (Conceptual)
Key Idea:
Partition the array similar to quicksort’s pivot step, treating evenness as the pivot condition.
Maintain a boundary index where all elements to the left are even.

Tradeoffs:
Simpler logic but may require extra space depending on implementation.

Intuition Behind the Optimal Solution
Why Two Pointers?
Avoids unnecessary moves by processing the array from both ends simultaneously.

Stability?
Order within even/odd groups isn’t preserved (not required by the problem).

Example Walkthrough
Input: [3, 1, 2, 4]
Swap 3 (odd @ left) and 4 (even @ right) → [4, 1, 2, 3]
Swap 1 (odd @ left) and 2 (even @ right) → [4, 2, 1, 3]
Result: Evens (4, 2) appear before odds (1, 3).

When to Use Each Approach
Approach	Best For	Tradeoffs
Two-Pointer	Space-constrained	Slightly complex logic
Partition-Based	Readability	Potential extra space
Recommendation: Default to the two-pointer method for interviews.

Related Problems
Move Zeroes (LeetCode #283)
Segregate Even and Odd (GFG)
