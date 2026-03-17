# Contains Duplicate

## Problem

Given an integer array `nums`, return `true` if any value appears at least twice, otherwise return `false`.

## Approach

Use a hash set to track seen elements while iterating through the array.

* For each number:

  * If it already exists in the set → duplicate found → return `true`
  * Otherwise, add it to the set

This avoids comparing every pair (which would be O(n²)) and instead leverages constant-time lookups.

## Key Insight

A hash set provides O(1) average lookup time, allowing us to detect duplicates in a single pass.

## Complexity

* Time: O(n)
* Space: O(n)

## Edge Cases

* Empty array → return `false`
* Single element → return `false`
* All elements identical → return `true`

## Improvements (optional)

* If memory is constrained, sorting the array first allows solving in O(n log n) time with O(1) extra space.
* Tradeoff: sorting mutates input and is slower than hashing.

## Example

Input: [1, 2, 3, 3]
Output: true

Input: [1, 2, 3, 4]
Output: false
