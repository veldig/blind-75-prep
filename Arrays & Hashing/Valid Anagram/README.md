# Valid Anagram

## Problem
Given two strings `s` and `t`, return `true` if `t` is an anagram of `s`, otherwise return `false`.

An anagram contains the exact same characters as another string, but possibly in a different order.

## Approach
Sort both strings and compare the results.

If two strings are anagrams, their sorted versions will be identical because they contain the same characters with the same frequencies.

This is a clean and simple solution for lowercase English letters.

## Key Insight
Anagrams differ only in character order, not character frequency. Sorting normalizes the order, making direct comparison possible.

## Complexity
- Time: O(n log n)
- Space: O(n)

## Edge Cases
- Different lengths → return `false`
- Same letters in different order → return `true`
- One mismatched character → return `false`
- Empty strings → return `true`

## Alternative Approach
A frequency-count approach using a hash map or `Counter` can solve this in O(n) time, at the cost of additional space.

## Example
Input: s = "racecar", t = "carrace"  
Output: true

Input: s = "jar", t = "jam"  
Output: false