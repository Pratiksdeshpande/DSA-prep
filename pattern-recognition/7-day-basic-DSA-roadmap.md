# 7-Day LeetCode DSA Roadmap

## Senior Software Developer / Senior Golang Developer

> **Duration:** 7 Days
> **Primary Language:** Go
> **Target:** Easy + foundational Medium problems
> **Focus:** Frequently asked DSA topics for Software/Senior Software Developer interviews

---

# 📌 How to Use This Roadmap

Each day contains:

* Core DSA topic
* Important concepts
* Must-do LeetCode problems
* Should-do LeetCode problems
* Optional problems
* Go-specific implementation practice
* Daily completion checklist

### Priority

| Priority     | Meaning                  |
| ------------ | ------------------------ |
| 🔴 Must Do   | Complete these problems  |
| 🟡 Should Do | Complete if time permits |
| 🟢 Optional  | Extra practice           |

---

# 📊 7-Day Overview

| Day   | Topics                              | Primary Focus                   |
| ----- | ----------------------------------- | ------------------------------- |
| Day 1 | Arrays + Hashing + Strings          | HashMap, HashSet, Frequency     |
| Day 2 | Two Pointers + Sliding Window       | Array/String windows            |
| Day 3 | Stack + Queue + Linked List         | Linear data structures          |
| Day 4 | Binary Search + Sorting + Intervals | Searching & ordering            |
| Day 5 | Binary Trees + BST                  | DFS, BFS, Recursion             |
| Day 6 | Heap + Graph + Backtracking         | Priority Queue, Graph traversal |
| Day 7 | Mixed Revision + Interview Set      | Consolidation + timed practice  |

---

# 📅 DAY 1 — Arrays, Hashing & Strings

## Topics

* Array traversal
* HashMap
* HashSet
* Frequency counting
* String manipulation
* Character frequency
* Prefix/suffix basics
* Single-pass array problems
* Kadane's Algorithm

---

## 🔴 Must Do

### 1. Two Sum

**LeetCode #1**

Difficulty: Easy

Topics:

```text
Array
HashMap
```

---

### 2. Contains Duplicate

**LeetCode #217**

Difficulty: Easy

Topics:

```text
Array
HashSet
```

---

### 3. Valid Anagram

**LeetCode #242**

Difficulty: Easy

Topics:

```text
String
HashMap
Frequency
```

---

### 4. Majority Element

**LeetCode #169**

Difficulty: Easy

Topics:

```text
Array
HashMap
Boyer-Moore Voting
```

---

### 5. Best Time to Buy and Sell Stock

**LeetCode #121**

Difficulty: Easy

Topics:

```text
Array
Greedy
Single Pass
```

---

### 6. Maximum Subarray

**LeetCode #53**

Difficulty: Medium

Topics:

```text
Array
Kadane's Algorithm
Dynamic Programming
```

> This is an important problem to understand even though it is classified as Medium.

---

## 🟡 Should Do

### 7. Missing Number

**LeetCode #268**

Topics:

```text
Array
Math
XOR
```

---

### 8. Single Number

**LeetCode #136**

Topics:

```text
Array
Bit Manipulation
XOR
```

---

### 9. Intersection of Two Arrays II

**LeetCode #350**

Topics:

```text
Array
HashMap
Sorting
```

---

### 10. Group Anagrams

**LeetCode #49**

Difficulty: Medium

Topics:

```text
String
HashMap
Sorting
Frequency
```

---

## 🟢 Optional

### 11. Contains Duplicate II

**LeetCode #219**

### 12. Happy Number

**LeetCode #202**

### 13. Ransom Note

**LeetCode #383**

---

## Go Practice

Implement:

```go
map[int]int
map[string]int
map[int]struct{}
```

Practice:

* Map insertion
* Map lookup
* Map deletion
* Frequency counting
* Iterating maps
* String → `[]byte`
* String → `[]rune`

---

## ✅ Day 1 Checklist

* [ ] Two Sum
* [ ] Contains Duplicate
* [ ] Valid Anagram
* [ ] Majority Element
* [ ] Best Time to Buy and Sell Stock
* [ ] Maximum Subarray
* [ ] Missing Number
* [ ] Single Number
* [ ] Intersection of Two Arrays II
* [ ] Group Anagrams
* [ ] Go HashMap practice
* [ ] Go string/rune practice

---

# 📅 DAY 2 — Two Pointers & Sliding Window

## Topics

* Two Pointers
* Fixed-size Sliding Window
* Variable-size Sliding Window
* String windows
* Array windows
* In-place array manipulation

---

## 🔴 Must Do

### 1. Valid Palindrome

**LeetCode #125**

Difficulty: Easy

Topics:

```text
String
Two Pointers
```

---

### 2. Two Sum II — Input Array Is Sorted

**LeetCode #167**

Difficulty: Medium

Topics:

```text
Array
Two Pointers
```

---

### 3. Remove Duplicates from Sorted Array

**LeetCode #26**

Difficulty: Easy

Topics:

```text
Array
Two Pointers
In-place
```

---

### 4. Move Zeroes

**LeetCode #283**

Difficulty: Easy

Topics:

```text
Array
Two Pointers
In-place
```

---

### 5. Maximum Average Subarray I

**LeetCode #643**

Difficulty: Easy

Topics:

```text
Array
Sliding Window
```

---

### 6. Longest Substring Without Repeating Characters

**LeetCode #3**

Difficulty: Medium

Topics:

```text
String
HashMap
Sliding Window
```

> One of the most important Sliding Window problems to learn.

---

### 7. Minimum Size Subarray Sum

**LeetCode #209**

Difficulty: Medium

Topics:

```text
Array
Sliding Window
```

---

## 🟡 Should Do

### 8. Merge Sorted Array

**LeetCode #88**

Difficulty: Easy

Topics:

```text
Array
Two Pointers
```

---

### 9. Squares of a Sorted Array

**LeetCode #977**

Difficulty: Easy

Topics:

```text
Array
Two Pointers
```

---

### 10. Valid Palindrome II

**LeetCode #680**

Difficulty: Easy

Topics:

```text
String
Two Pointers
```

---

## 🟢 Optional

### 11. Longest Repeating Character Replacement

**LeetCode #424**

Difficulty: Medium

Topics:

```text
String
Sliding Window
HashMap
```

---

### 12. Permutation in String

**LeetCode #567**

Difficulty: Medium

Topics:

```text
String
Sliding Window
Frequency
```

---

### 13. Container With Most Water

**LeetCode #11**

Difficulty: Medium

Topics:

```text
Array
Two Pointers
Greedy
```

---

## Go Practice

Implement:

```text
Two-pointer traversal
Sliding-window traversal
In-place modification
```

Practice:

```go
left := 0
right := len(nums) - 1
```

and:

```go
left := 0

for right := 0; right < len(nums); right++ {
    // window logic
}
```

---

## ✅ Day 2 Checklist

* [ ] Valid Palindrome
* [ ] Two Sum II
* [ ] Remove Duplicates
* [ ] Move Zeroes
* [ ] Maximum Average Subarray I
* [ ] Longest Substring Without Repeating Characters
* [ ] Minimum Size Subarray Sum
* [ ] Merge Sorted Array
* [ ] Squares of a Sorted Array
* [ ] Valid Palindrome II
* [ ] Go Two Pointer implementation
* [ ] Go Sliding Window implementation

---

# 📅 DAY 3 — Stack, Queue & Linked List

## Topics

* Stack
* Queue
* Monotonic Stack
* Linked List
* Pointer manipulation
* Fast/Slow pointers
* Linked List reversal

---

# Stack

## 🔴 Must Do

### 1. Valid Parentheses

**LeetCode #20**

Difficulty: Easy

Topics:

```text
Stack
String
```

---

### 2. Min Stack

**LeetCode #155**

Difficulty: Medium

Topics:

```text
Stack
Design
```

---

### 3. Evaluate Reverse Polish Notation

**LeetCode #150**

Difficulty: Medium

Topics:

```text
Stack
```

---

### 4. Next Greater Element I

**LeetCode #496**

Difficulty: Easy

Topics:

```text
Stack
Monotonic Stack
HashMap
```

---

### 5. Daily Temperatures

**LeetCode #739**

Difficulty: Medium

Topics:

```text
Stack
Monotonic Stack
```

---

# Linked List

## 🔴 Must Do

### 6. Reverse Linked List

**LeetCode #206**

Difficulty: Easy

Topics:

```text
Linked List
Pointers
```

---

### 7. Middle of the Linked List

**LeetCode #876**

Difficulty: Easy

Topics:

```text
Linked List
Fast/Slow Pointer
```

---

### 8. Linked List Cycle

**LeetCode #141**

Difficulty: Easy

Topics:

```text
Linked List
Fast/Slow Pointer
```

---

### 9. Merge Two Sorted Lists

**LeetCode #21**

Difficulty: Easy

Topics:

```text
Linked List
Two Pointers
```

---

## 🟡 Should Do

### 10. Remove Linked List Elements

**LeetCode #203**

Difficulty: Easy

---

### 11. Palindrome Linked List

**LeetCode #234**

Difficulty: Easy

Topics:

```text
Linked List
Fast/Slow Pointer
Reverse Linked List
```

---

### 12. Intersection of Two Linked Lists

**LeetCode #160**

Difficulty: Easy

Topics:

```text
Linked List
Two Pointers
```

---

## 🟢 Optional

### 13. Add Two Numbers

**LeetCode #2**

Difficulty: Medium

---

### 14. Remove Nth Node From End of List

**LeetCode #19**

Difficulty: Medium

Topics:

```text
Linked List
Two Pointers
```

---

## Go Practice

Implement:

```go
type ListNode struct {
    Val  int
    Next *ListNode
}
```

Practice:

* Creating nodes
* Traversing
* Reversing
* Inserting
* Deleting
* Fast/slow pointers

---

## Queue Practice

Implement a queue using:

```go
[]int
```

Understand:

```text
enqueue
dequeue
front
back
```

---

## ✅ Day 3 Checklist

* [ ] Valid Parentheses
* [ ] Min Stack
* [ ] Reverse Polish Notation
* [ ] Next Greater Element I
* [ ] Daily Temperatures
* [ ] Reverse Linked List
* [ ] Middle of Linked List
* [ ] Linked List Cycle
* [ ] Merge Two Sorted Lists
* [ ] Remove Linked List Elements
* [ ] Palindrome Linked List
* [ ] Intersection of Two Linked Lists
* [ ] Go Stack
* [ ] Go Queue
* [ ] Go Linked List

---

# 📅 DAY 4 — Binary Search, Sorting & Intervals

## Topics

* Binary Search
* Search space
* Lower/upper bound concepts
* Rotated sorted arrays
* Sorting
* Intervals
* Sorting + Greedy

---

# Binary Search

## 🔴 Must Do

### 1. Binary Search

**LeetCode #704**

Difficulty: Easy

---

### 2. Search Insert Position

**LeetCode #35**

Difficulty: Easy

---

### 3. First Bad Version

**LeetCode #278**

Difficulty: Easy

---

### 4. Find Minimum in Rotated Sorted Array

**LeetCode #153**

Difficulty: Medium

---

## 🟡 Should Do

### 5. Search in Rotated Sorted Array

**LeetCode #33**

Difficulty: Medium

---

### 6. Sqrt(x)

**LeetCode #69**

Difficulty: Easy

Topics:

```text
Binary Search
```

---

### 7. Valid Perfect Square

**LeetCode #367**

Difficulty: Easy

---

# Sorting

Understand and implement at least once:

* Bubble Sort
* Selection Sort
* Insertion Sort
* Merge Sort
* Quick Sort

---

# Intervals

## 🔴 Must Do

### 8. Merge Intervals

**LeetCode #56**

Difficulty: Medium

Topics:

```text
Sorting
Intervals
```

---

### 9. Insert Interval

**LeetCode #57**

Difficulty: Medium

---

## 🟡 Should Do

### 10. Meeting Rooms

**LeetCode #252**

Difficulty: Easy

---

### 11. Meeting Rooms II

**LeetCode #253**

Difficulty: Medium

Topics:

```text
Intervals
Sorting
Heap
```

---

## Go Practice

Know:

```go
sort.Ints(nums)
```

and:

```go
sort.Slice(intervals, func(i, j int) bool {
    return intervals[i][0] < intervals[j][0]
})
```

---

## ✅ Day 4 Checklist

* [ ] Binary Search
* [ ] Search Insert Position
* [ ] First Bad Version
* [ ] Sqrt(x)
* [ ] Valid Perfect Square
* [ ] Find Minimum in Rotated Sorted Array
* [ ] Search in Rotated Sorted Array
* [ ] Merge Intervals
* [ ] Insert Interval
* [ ] Meeting Rooms
* [ ] Meeting Rooms II
* [ ] Bubble Sort
* [ ] Selection Sort
* [ ] Insertion Sort
* [ ] Merge Sort
* [ ] Quick Sort
* [ ] Go `sort` package

---

# 📅 DAY 5 — Binary Trees & BST

## Topics

* Binary Tree
* BST
* DFS
* BFS
* Recursion
* Tree traversal
* Tree depth/height
* Level-order traversal

---

# 🔴 Must Do

### 1. Maximum Depth of Binary Tree

**LeetCode #104**

Difficulty: Easy

---

### 2. Same Tree

**LeetCode #100**

Difficulty: Easy

---

### 3. Invert Binary Tree

**LeetCode #226**

Difficulty: Easy

---

### 4. Binary Tree Preorder Traversal

**LeetCode #144**

Difficulty: Easy

---

### 5. Binary Tree Inorder Traversal

**LeetCode #94**

Difficulty: Easy

---

### 6. Binary Tree Level Order Traversal

**LeetCode #102**

Difficulty: Medium

---

### 7. Search in a Binary Search Tree

**LeetCode #700**

Difficulty: Easy

---

### 8. Minimum Depth of Binary Tree

**LeetCode #111**

Difficulty: Easy

---

## 🟡 Should Do

### 9. Symmetric Tree

**LeetCode #101**

Difficulty: Easy

---

### 10. Balanced Binary Tree

**LeetCode #110**

Difficulty: Easy

---

### 11. Path Sum

**LeetCode #112**

Difficulty: Easy

---

### 12. Lowest Common Ancestor of a Binary Search Tree

**LeetCode #235**

Difficulty: Medium

---

## 🟢 Optional

### 13. Diameter of Binary Tree

**LeetCode #543**

Difficulty: Easy

---

### 14. Subtree of Another Tree

**LeetCode #572**

Difficulty: Easy

---

## Go Practice

Implement:

```go
type TreeNode struct {
    Val   int
    Left  *TreeNode
    Right *TreeNode
}
```

Implement:

```text
DFS Recursive
DFS Iterative
BFS
```

---

## ✅ Day 5 Checklist

* [ ] Maximum Depth
* [ ] Same Tree
* [ ] Invert Binary Tree
* [ ] Preorder Traversal
* [ ] Inorder Traversal
* [ ] Level Order Traversal
* [ ] Search BST
* [ ] Minimum Depth
* [ ] Symmetric Tree
* [ ] Balanced Binary Tree
* [ ] Path Sum
* [ ] LCA of BST
* [ ] Diameter of Binary Tree
* [ ] Go TreeNode implementation
* [ ] Recursive DFS
* [ ] Iterative DFS
* [ ] BFS

---

# 📅 DAY 6 — Heap, Graph & Backtracking

## Topics

* Heap
* Priority Queue
* DFS on Graph
* BFS on Graph
* Grid traversal
* Connected Components
* Basic Backtracking

---

# Heap

## 🔴 Must Do

### 1. Kth Largest Element in an Array

**LeetCode #215**

Difficulty: Medium

Topics:

```text
Heap
Quickselect
```

---

### 2. Last Stone Weight

**LeetCode #1046**

Difficulty: Easy

Topics:

```text
Max Heap
```

---

### 3. Kth Largest Element in a Stream

**LeetCode #703**

Difficulty: Easy

Topics:

```text
Min Heap
```

---

### 4. Top K Frequent Elements

**LeetCode #347**

Difficulty: Medium

Topics:

```text
HashMap
Heap
```

---

# Graph

## 🔴 Must Do

### 5. Find if Path Exists in Graph

**LeetCode #1971**

Difficulty: Easy

Topics:

```text
Graph
DFS
BFS
```

---

### 6. Number of Islands

**LeetCode #200**

Difficulty: Medium

Topics:

```text
Grid
DFS
BFS
```

---

### 7. Flood Fill

**LeetCode #733**

Difficulty: Easy

Topics:

```text
DFS
BFS
Grid
```

---

### 8. Number of Connected Components in an Undirected Graph

**LeetCode #323**

Difficulty: Medium

Topics:

```text
Graph
DFS
BFS
Union Find
```

---

# Backtracking

## 🟡 Should Do

### 9. Subsets

**LeetCode #78**

Difficulty: Medium

---

### 10. Permutations

**LeetCode #46**

Difficulty: Medium

---

## 🟢 Optional

### 11. Combination Sum

**LeetCode #39**

Difficulty: Medium

---

## Go Practice

### Heap

Learn:

```go
container/heap
```

Implement:

```text
Min Heap
Max Heap
Heap of custom structs
```

---

### Graph

Implement adjacency list:

```go
graph := make(map[int][]int)
```

Practice:

```text
DFS
BFS
Visited Set
```

---

## ✅ Day 6 Checklist

* [ ] Kth Largest Element
* [ ] Last Stone Weight
* [ ] Kth Largest in Stream
* [ ] Top K Frequent Elements
* [ ] Find if Path Exists
* [ ] Number of Islands
* [ ] Flood Fill
* [ ] Connected Components
* [ ] Subsets
* [ ] Permutations
* [ ] Go Min Heap
* [ ] Go Max Heap
* [ ] Go Graph
* [ ] DFS
* [ ] BFS

---

# 📅 DAY 7 — Revision + Mixed LeetCode Interview Set

## 🎯 Objective

Day 7 is your **assessment and consolidation day**.

Do not spend the day learning new DSA topics.

---

# Round 1 — Arrays / Hashing

### 🔴 Must Do

#### 1. Two Sum

**#1**

#### 2. Best Time to Buy and Sell Stock

**#121**

#### 3. Maximum Subarray

**#53**

---

# Round 2 — Two Pointers / Sliding Window

### 🔴 Must Do

#### 4. Valid Palindrome

**#125**

#### 5. Longest Substring Without Repeating Characters

**#3**

---

# Round 3 — Stack / Linked List

### 🔴 Must Do

#### 6. Valid Parentheses

**#20**

#### 7. Reverse Linked List

**#206**

#### 8. Linked List Cycle

**#141**

---

# Round 4 — Binary Search

### 🔴 Must Do

#### 9. Binary Search

**#704**

#### 10. Search Insert Position

**#35**

---

# Round 5 — Trees

### 🔴 Must Do

#### 11. Maximum Depth of Binary Tree

**#104**

#### 12. Binary Tree Level Order Traversal

**#102**

---

# Round 6 — Heap / Graph

### 🔴 Must Do

#### 13. Kth Largest Element in an Array

**#215**

#### 14. Number of Islands

**#200**

---

# Round 7 — Backtracking

### 🟡 Should Do

#### 15. Subsets

**#78**

---

# ⏱️ Day 7 Timed Practice

For each problem:

```text
Easy:
20 minutes

Medium:
25–30 minutes
```

Target:

```text
3–5 problems in one sitting
```

Then review the remaining problems.

---

# 📊 Final 7-Day Problem Tracker

## Day 1

|  # | Problem                         | Priority | Done |
| -: | ------------------------------- | :------: | :--: |
|  1 | Two Sum                         |    🔴    |  [ ] |
|  2 | Contains Duplicate              |    🔴    |  [ ] |
|  3 | Valid Anagram                   |    🔴    |  [ ] |
|  4 | Majority Element                |    🔴    |  [ ] |
|  5 | Best Time to Buy and Sell Stock |    🔴    |  [ ] |
|  6 | Maximum Subarray                |    🔴    |  [ ] |
|  7 | Missing Number                  |    🟡    |  [ ] |
|  8 | Single Number                   |    🟡    |  [ ] |
|  9 | Intersection of Two Arrays II   |    🟡    |  [ ] |
| 10 | Group Anagrams                  |    🟡    |  [ ] |

---

## Day 2

|  # | Problem                                        | Priority | Done |
| -: | ---------------------------------------------- | :------: | :--: |
|  1 | Valid Palindrome                               |    🔴    |  [ ] |
|  2 | Two Sum II                                     |    🔴    |  [ ] |
|  3 | Remove Duplicates from Sorted Array            |    🔴    |  [ ] |
|  4 | Move Zeroes                                    |    🔴    |  [ ] |
|  5 | Maximum Average Subarray I                     |    🔴    |  [ ] |
|  6 | Longest Substring Without Repeating Characters |    🔴    |  [ ] |
|  7 | Minimum Size Subarray Sum                      |    🔴    |  [ ] |
|  8 | Merge Sorted Array                             |    🟡    |  [ ] |
|  9 | Squares of a Sorted Array                      |    🟡    |  [ ] |
| 10 | Valid Palindrome II                            |    🟡    |  [ ] |
| 11 | Longest Repeating Character Replacement        |    🟢    |  [ ] |
| 12 | Container With Most Water                      |    🟢    |  [ ] |

---

## Day 3

|  # | Problem                          | Priority | Done |
| -: | -------------------------------- | :------: | :--: |
|  1 | Valid Parentheses                |    🔴    |  [ ] |
|  2 | Min Stack                        |    🔴    |  [ ] |
|  3 | Evaluate Reverse Polish Notation |    🔴    |  [ ] |
|  4 | Next Greater Element I           |    🔴    |  [ ] |
|  5 | Daily Temperatures               |    🔴    |  [ ] |
|  6 | Reverse Linked List              |    🔴    |  [ ] |
|  7 | Middle of the Linked List        |    🔴    |  [ ] |
|  8 | Linked List Cycle                |    🔴    |  [ ] |
|  9 | Merge Two Sorted Lists           |    🔴    |  [ ] |
| 10 | Remove Linked List Elements      |    🟡    |  [ ] |
| 11 | Palindrome Linked List           |    🟡    |  [ ] |
| 12 | Intersection of Two Linked Lists |    🟡    |  [ ] |

---

## Day 4

|  # | Problem                              | Priority | Done |
| -: | ------------------------------------ | :------: | :--: |
|  1 | Binary Search                        |    🔴    |  [ ] |
|  2 | Search Insert Position               |    🔴    |  [ ] |
|  3 | First Bad Version                    |    🔴    |  [ ] |
|  4 | Sqrt(x)                              |    🟡    |  [ ] |
|  5 | Valid Perfect Square                 |    🟡    |  [ ] |
|  6 | Find Minimum in Rotated Sorted Array |    🔴    |  [ ] |
|  7 | Search in Rotated Sorted Array       |    🟡    |  [ ] |
|  8 | Merge Intervals                      |    🔴    |  [ ] |
|  9 | Insert Interval                      |    🔴    |  [ ] |
| 10 | Meeting Rooms                        |    🟡    |  [ ] |
| 11 | Meeting Rooms II                     |    🟡    |  [ ] |

---

## Day 5

|  # | Problem                      | Priority | Done |
| -: | ---------------------------- | :------: | :--: |
|  1 | Maximum Depth of Binary Tree |    🔴    |  [ ] |
|  2 | Same Tree                    |    🔴    |  [ ] |
|  3 | Invert Binary Tree           |    🔴    |  [ ] |
|  4 | Preorder Traversal           |    🔴    |  [ ] |
|  5 | Inorder Traversal            |    🔴    |  [ ] |
|  6 | Level Order Traversal        |    🔴    |  [ ] |
|  7 | Search in BST                |    🔴    |  [ ] |
|  8 | Minimum Depth                |    🔴    |  [ ] |
|  9 | Symmetric Tree               |    🟡    |  [ ] |
| 10 | Balanced Binary Tree         |    🟡    |  [ ] |
| 11 | Path Sum                     |    🟡    |  [ ] |
| 12 | LCA of BST                   |    🟡    |  [ ] |
| 13 | Diameter of Binary Tree      |    🟢    |  [ ] |

---

## Day 6

|  # | Problem                 | Priority | Done |
| -: | ----------------------- | :------: | :--: |
|  1 | Kth Largest Element     |    🔴    |  [ ] |
|  2 | Last Stone Weight       |    🔴    |  [ ] |
|  3 | Kth Largest in Stream   |    🔴    |  [ ] |
|  4 | Top K Frequent Elements |    🔴    |  [ ] |
|  5 | Find if Path Exists     |    🔴    |  [ ] |
|  6 | Number of Islands       |    🔴    |  [ ] |
|  7 | Flood Fill              |    🔴    |  [ ] |
|  8 | Connected Components    |    🔴    |  [ ] |
|  9 | Subsets                 |    🟡    |  [ ] |
| 10 | Permutations            |    🟡    |  [ ] |
| 11 | Combination Sum         |    🟢    |  [ ] |

---

## Day 7

|  # | Problem                                        | Priority | Done |
| -: | ---------------------------------------------- | :------: | :--: |
|  1 | Two Sum                                        |    🔴    |  [ ] |
|  2 | Best Time to Buy and Sell Stock                |    🔴    |  [ ] |
|  3 | Maximum Subarray                               |    🔴    |  [ ] |
|  4 | Valid Palindrome                               |    🔴    |  [ ] |
|  5 | Longest Substring Without Repeating Characters |    🔴    |  [ ] |
|  6 | Valid Parentheses                              |    🔴    |  [ ] |
|  7 | Reverse Linked List                            |    🔴    |  [ ] |
|  8 | Linked List Cycle                              |    🔴    |  [ ] |
|  9 | Binary Search                                  |    🔴    |  [ ] |
| 10 | Search Insert Position                         |    🔴    |  [ ] |
| 11 | Maximum Depth of Binary Tree                   |    🔴    |  [ ] |
| 12 | Level Order Traversal                          |    🔴    |  [ ] |
| 13 | Kth Largest Element                            |    🔴    |  [ ] |
| 14 | Number of Islands                              |    🔴    |  [ ] |
| 15 | Subsets                                        |    🟡    |  [ ] |

---

# 📈 Overall Progress

## Day Completion

* [ ] Day 1 — Arrays / Hashing / Strings
* [ ] Day 2 — Two Pointers / Sliding Window
* [ ] Day 3 — Stack / Queue / Linked List
* [ ] Day 4 — Binary Search / Sorting / Intervals
* [ ] Day 5 — Trees / BST
* [ ] Day 6 — Heap / Graph / Backtracking
* [ ] Day 7 — Revision / Mock Interview

---

# 🎯 Minimum Target

If time is limited, prioritize **all 🔴 problems first**.

The minimum target is approximately:

```text
Day 1 → 6 problems
Day 2 → 7 problems
Day 3 → 9 problems
Day 4 → 9 problems
Day 5 → 8 problems
Day 6 → 8 problems
Day 7 → 10+ revision problems
```

This gives approximately:

```text
50+ focused problem attempts
```

across the week, with repeated exposure to the most important basic DSA structures.

---

# 🧑‍💻 Go Implementation Checklist

By the end of the 7 days, I should have implemented these at least once in Go:

* [ ] HashMap-based solution
* [ ] HashSet using `map`
* [ ] Two Pointers
* [ ] Sliding Window
* [ ] Stack using slice
* [ ] Queue using slice
* [ ] Linked List
* [ ] Fast/Slow Pointer
* [ ] Binary Search
* [ ] Merge Sort
* [ ] Quick Sort
* [ ] TreeNode
* [ ] Recursive DFS
* [ ] Iterative DFS
* [ ] BFS
* [ ] Min Heap
* [ ] Max Heap
* [ ] Graph using adjacency list
* [ ] Graph DFS
* [ ] Graph BFS
* [ ] Backtracking

---

# 🏁 7-Day Completion Criteria

At the end of the week:

```text
Total Days Completed:       __ / 7

Must-Do Problems:           __ / __

Should-Do Problems:         __ / __

Optional Problems:          __ / __

Go Implementations:         __ / __

Mock Problems Solved:       __ / __
```

### Topics Completed

* [ ] Arrays
* [ ] Strings
* [ ] HashMap
* [ ] HashSet
* [ ] Two Pointers
* [ ] Sliding Window
* [ ] Stack
* [ ] Queue
* [ ] Linked List
* [ ] Binary Search
* [ ] Sorting
* [ ] Intervals
* [ ] Binary Tree
* [ ] BST
* [ ] DFS
* [ ] BFS
* [ ] Heap
* [ ] Graph
* [ ] Backtracking

---

# 🚀 Next Roadmap After Day 7

After completing this 7-day roadmap, the next stage should be:

```text
7-Day Foundation
       ↓
Pattern-Based Easy Problems
       ↓
Easy → Medium Problems
       ↓
Advanced Sliding Window
       ↓
Advanced Binary Search
       ↓
Greedy
       ↓
Dynamic Programming
       ↓
Advanced Graphs
       ↓
Trie / Union Find
       ↓
Senior-Level Mixed Problems
       ↓
Timed Mock Interviews
```

The goal of this 7-day phase is to build a **strong basic DSA foundation in Go** before moving into the medium/harder problems expected in senior-level interviews.
