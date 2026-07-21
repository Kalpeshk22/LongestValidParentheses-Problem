# Longest Valid Parentheses

## Problem Statement

Given a string containing only '(' and ')' return the length of the longest valid (well formed) parentheses substring.

## Solution

This solution uses a **Stack** to keep track of the indices of parentheses.

### Algorithm
1. Push `-1` into the stack as the base index
2. Traverse the string character by character
3. If the current character is `'('`, push its index onto the stack
4. If the current character is `')'`:
   - Pop the top element.
   - If the stack becomes empty, push the current index
   - Otherwise, calculate the current valid substring length using
     
     currentLength = currentIndex - stack.peek()

   - Update the maximum length.

## Time Complexity

- **O(n)**

## Space Complexity

- **O(n)**

## Sample Input & Output

### Input

java
System.out.println(longestValidParentheses("(()"));
System.out.println(longestValidParentheses(")()())"));
System.out.println(longestValidParentheses(""));


### Output

2
4
0

## Language

Java
