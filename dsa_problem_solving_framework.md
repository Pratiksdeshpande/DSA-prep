# DSA Problem Solving & Pattern Recognition Framework

> A systematic framework to identify the right data structure, algorithm, and problem-solving pattern before writing code.

---

# 1. The Real Problem With DSA

When solving DSA problems, many people follow this approach:

```text
Read problem
    ↓
Try to understand it
    ↓
Start coding
    ↓
Get stuck
    ↓
Look at solution
```

This approach creates **solution dependency**.

The goal should instead be:

```text
Read Problem
    ↓
Understand the problem
    ↓
Extract constraints
    ↓
Identify the mathematical / structural property
    ↓
Generate possible approaches
    ↓
Eliminate approaches using constraints
    ↓
Recognize the pattern
    ↓
Choose Data Structure
    ↓
Choose Algorithm
    ↓
Prove correctness
    ↓
Analyze complexity
    ↓
Implement
    ↓
Test edge cases
```

The most important skill is therefore:

# Pattern Recognition

You should eventually be able to look at a problem and think:

```text
"Contiguous subarray + condition on sum"
        ↓
Sliding Window / Prefix Sum

"Need nearest greater element"
        ↓
Monotonic Stack

"Repeatedly need minimum element"
        ↓
Heap / Priority Queue

"Connected components"
        ↓
Graph / DFS / BFS / Union-Find

"All combinations / choices"
        ↓
Backtracking

"Optimal answer + overlapping subproblems"
        ↓
Dynamic Programming
```

---

# 2. The Golden Rule

Never ask:

> "Which algorithm do I remember that solves this?"

Instead ask:

> "What property of this problem determines the algorithm?"

For example:

```text
Problem:
Find the longest substring without repeating characters.

Bad thinking:
"I remember this problem. Use HashMap."

Better thinking:
- It is a substring → contiguous range
- We need the longest range satisfying a condition
- Condition: no duplicate characters
- We need to maintain a valid range
- When the range becomes invalid, shrink it
- Therefore → Sliding Window
- Need fast duplicate detection → HashMap / Set
```

This distinction is extremely important.

---

# 3. Step 1 — Read the Problem Without Thinking About Code

On your first read, do NOT think about:

* arrays
* maps
* recursion
* DP
* loops
* code

First understand:

### What is the problem actually asking?

Rewrite the problem in your own words.

For example:

> Given an array, find the maximum sum of a contiguous subarray.

Rewrite:

```text
I need to choose one continuous portion of the array
and maximize the sum of its elements.
```

Immediately, the word:

```text
CONTIGUOUS
```

becomes important.

It tells you that the problem is about a **range/window**.

---

# 4. Step 2 — Identify the Input Structure

Ask:

### What kind of data am I given?

Common structures:

| Input            | Possible Direction                                               |
| ---------------- | ---------------------------------------------------------------- |
| Array            | Two pointers, Sliding Window, Prefix Sum, Binary Search, Sorting |
| String           | Sliding Window, HashMap, Stack, Two Pointers                     |
| Linked List      | Two Pointers, Fast/Slow Pointer                                  |
| Tree             | DFS, BFS, Recursion                                              |
| Graph            | DFS, BFS, Dijkstra, Union-Find, Topological Sort                 |
| Matrix           | DFS/BFS, Dynamic Programming, Prefix Sum                         |
| Intervals        | Sorting, Greedy, Sweep Line                                      |
| Stream of values | Heap, HashMap, Sliding Window                                    |
| Set of choices   | Backtracking / DP                                                |
| Dependencies     | Graph / Topological Sort                                         |

Do not choose the algorithm yet.

Just classify the structure.

---

# 5. Step 3 — Identify the Output

Ask:

### What exactly must I return?

Typical outputs:

```text
Boolean
    ↓
Does a valid solution exist?

Integer
    ↓
Count / minimum / maximum / length

Array
    ↓
Actual elements / positions / result sequence

String
    ↓
Constructed result

List of solutions
    ↓
Backtracking / enumeration

Graph / ordering
    ↓
Traversal / Topological Sort / Shortest Path
```

Output type gives you an early clue.

---

# 6. Step 4 — Identify the Operation

This is one of the strongest pattern-recognition techniques.

Ask:

> What operation is the problem repeatedly asking me to perform?

Examples:

### Search

```text
Find whether X exists
Find position of X
Find first/last occurrence
```

Possible:

```text
HashMap
Binary Search
Two Pointers
```

---

### Minimum / Maximum

```text
Find minimum
Find maximum
Find kth smallest/largest
```

Possible:

```text
Sorting
Heap
Monotonic Stack
Dynamic Programming
Greedy
```

---

### Frequency

```text
Count occurrences
Find duplicates
Most frequent element
Anagram
```

Think:

```text
HashMap / Frequency Array
```

---

### Nearest Element

```text
Next greater element
Previous smaller element
Nearest larger value
```

Think:

```text
Monotonic Stack
```

---

### Connectivity

```text
Are two nodes connected?
How many components?
Can we reach X?
```

Think:

```text
DFS
BFS
Union-Find
```

---

### Dependencies

```text
A must happen before B.
```

Think:

```text
Directed Graph
Topological Sort
```

---

# 7. Step 5 — Identify the Constraints

This is arguably the most important step.

Never ignore constraints.

Suppose:

```text
N <= 10
```

You can potentially use:

```text
O(2^N)
O(N!)
```

---

If:

```text
N <= 20
```

You may consider:

```text
O(2^N)
Bitmasking
Backtracking
Meet in the Middle
```

---

If:

```text
N <= 100
```

Potentially:

```text
O(N^2)
O(N^3)
```

depending on the problem.

---

If:

```text
N <= 10^5
```

Usually avoid:

```text
O(N^2)
```

Prefer:

```text
O(N)
O(N log N)
```

---

If:

```text
N <= 10^6
```

Usually target:

```text
O(N)
```

or close to it.

---

If:

```text
N <= 10^9
```

You probably cannot iterate through all values.

Think about:

```text
Binary Search
Mathematical Observation
Logarithmic Algorithm
Digit / Bit manipulation
Number theory
```

---

# 8. Complexity Constraint Cheat Sheet

|            N | Usually Consider            |
| -----------: | --------------------------- |
|        <= 10 | O(N!), O(2^N), Backtracking |
|        <= 20 | O(2^N), Bitmasking          |
|        <= 50 | O(N^3), sometimes O(2^N)    |
|       <= 100 | O(N^3), O(N^2)              |
|     <= 1,000 | O(N^2), O(N² log N)         |
|    <= 10,000 | O(N²) sometimes             |
|   <= 100,000 | O(N log N), O(N)            |
| <= 1,000,000 | O(N), O(N log N) carefully  |
|      >= 10^9 | O(log N), mathematical      |

These are guidelines, not absolute rules.

---

# 9. Step 6 — Ask: Is Order Important?

This single question eliminates many possibilities.

## Case 1: Order matters

Example:

```text
[1, 2, 3, 4]
```

You need:

```text
subarray
substring
subsequence
```

Think about:

```text
Two Pointers
Sliding Window
Prefix Sum
Dynamic Programming
```

---

## Case 2: Order does not matter

You may consider:

```text
Sorting
Hashing
Sets
Combinations
Greedy
```

---

# 10. Subarray vs Subsequence vs Subset

This distinction is critical.

## Subarray

Elements must be:

```text
CONTIGUOUS
```

Example:

```text
[1, 2, 3, 4]

[2, 3]     ✓
[1, 2, 3]  ✓
[1, 3]     ✗
```

Common patterns:

```text
Sliding Window
Prefix Sum
Kadane's Algorithm
Monotonic Queue
HashMap + Prefix Sum
```

---

## Subsequence

Elements maintain order but don't need to be contiguous.

```text
[1, 2, 3, 4]

[1, 3] ✓
[2, 4] ✓
```

Common patterns:

```text
Dynamic Programming
Two Pointers
Greedy
```

---

## Subset

Order does not matter.

```text
[1, 2, 3]

{1,3}
{2}
{1,2,3}
```

Common patterns:

```text
Backtracking
Bitmasking
Dynamic Programming
```

---

# 11. Step 7 — Look for Keywords

Problem statements often contain pattern signals.

## Sliding Window Signals

Look for:

```text
subarray
substring
contiguous
longest
shortest
maximum length
minimum length
at most K
at least K
exactly K
window
```

Example:

```text
Find the longest substring containing at most K distinct characters.
```

Recognition:

```text
substring
+
longest
+
constraint on current range
        ↓
Sliding Window
```

---

# 12. Sliding Window Decision Tree

Ask:

### Is it contiguous?

```text
YES
 ↓
Is the answer about a range/window?
 ↓
YES
 ↓
Can I expand/shrink the range while maintaining a condition?
 ↓
YES
 ↓
Sliding Window
```

Typical structure:

```text
left = 0

for right := 0; right < n; right++ {

    // Add arr[right]

    for window is invalid {
        // Remove arr[left]
        left++
    }

    // Update answer
}
```

---

# 13. Two Pointers Signals

Think Two Pointers when you see:

```text
sorted array
pair
two elements
remove duplicates
opposite ends
left/right
in-place
partition
```

Example:

```text
Find two numbers whose sum equals target.
```

If sorted:

```text
left → 
       [ ... ]
             ← right
```

Then:

```text
sum < target → left++

sum > target → right--

sum == target → found
```

---

# 14. HashMap Signals

Think HashMap when you need:

```text
frequency
count
duplicate detection
lookup
complement
mapping
grouping
visited state
```

Example:

```text
Two Sum
```

Recognition:

```text
For every x,
need target - x
```

Therefore:

```text
HashMap[value] = index
```

---

# 15. Prefix Sum Signals

Look for:

```text
subarray sum
range sum
sum between i and j
number of subarrays
sum equals K
```

Core idea:

```text
prefix[i] = sum of elements before/through i
```

For:

```text
sum(i...j)
```

we can calculate:

```text
prefix[j] - prefix[i-1]
```

This converts repeated range-sum computation from:

```text
O(N)
```

to:

```text
O(1)
```

after preprocessing.

---

# 16. Prefix Sum + HashMap

This is a very important combination.

Problem:

```text
Count subarrays whose sum equals K.
```

Think:

```text
Subarray
+
Sum
+
Count
```

Therefore:

```text
Prefix Sum
+
HashMap
```

Mathematical observation:

```text
prefix[j] - prefix[i] = K
```

Therefore:

```text
prefix[i] = prefix[j] - K
```

So while traversing:

```text
currentPrefix

need = currentPrefix - K
```

Look up:

```text
frequency[need]
```

This is a classic example of:

> **Algorithm pattern + data structure**

---

# 17. Binary Search Signals

Do not limit Binary Search to:

```text
"Find element in sorted array."
```

Binary Search is much more powerful.

Look for:

```text
sorted
monotonic
minimum possible
maximum possible
capacity
speed
time
answer range
feasibility
```

Especially:

> Find the minimum X such that a condition becomes true.

Example:

```text
Minimum capacity required to ship packages within D days.
```

Think:

```text
Possible capacity:

1 2 3 4 5 6 7 8 9 ...
        F F F T T T T
```

This is:

```text
Binary Search on Answer
```

---

# 18. Stack Signals

Think Stack when the problem involves:

```text
matching
nested
parentheses
undo
previous
next
nearest
monotonic
```

Examples:

```text
Valid Parentheses
Daily Temperatures
Next Greater Element
Largest Rectangle in Histogram
```

---

# 19. Monotonic Stack Signals

This deserves special attention.

Whenever you see:

```text
next greater
next smaller
previous greater
previous smaller
nearest greater
nearest smaller
```

Immediately think:

```text
Monotonic Stack
```

Example:

```text
[2, 1, 5, 3, 4]
```

Question:

```text
Next greater element
```

Instead of comparing every pair:

```text
O(N²)
```

maintain a stack with a monotonic property:

```text
O(N)
```

---

# 20. Heap / Priority Queue Signals

Think Heap when you repeatedly need:

```text
minimum
maximum
k smallest
k largest
top K
median
schedule next task
process highest priority
```

Examples:

```text
Top K Frequent Elements
Kth Largest Element
Merge K Sorted Lists
Meeting Rooms
Task Scheduling
```

Key question:

> Do I repeatedly need the smallest/largest element while the rest of the data is still changing?

If yes:

```text
Heap
```

---

# 21. Greedy Signals

Greedy problems usually contain:

```text
maximize
minimize
choose
earliest
latest
locally optimal
minimum number
maximum number
```

But keywords alone are NOT enough.

You need an **exchange argument / greedy-choice property**.

Example:

```text
Activity Selection
```

Choose the activity that finishes earliest.

Why?

Because finishing earliest leaves maximum remaining space for future activities.

The important skill is not:

> "This looks like Greedy."

It is:

> "Why is this local choice safe?"

---

# 22. Intervals Signals

If the input looks like:

```text
[start, end]
```

think:

```text
Intervals
```

Then usually:

```text
Sort by start
or
Sort by end
```

Typical problems:

```text
Merge Intervals
Insert Interval
Meeting Rooms
Meeting Rooms II
Minimum Number of Rooms
Interval Scheduling
```

Common pattern:

```text
Sort
+
Greedy / Heap
```

---

# 23. Linked List Signals

Typical signals:

```text
reverse
cycle
middle
nth from end
intersection
merge
```

Think:

```text
Fast / Slow Pointer
Two Pointers
In-place manipulation
```

Examples:

```text
Find cycle
        ↓
Fast + Slow

Find middle
        ↓
Fast + Slow

Nth node from end
        ↓
Two pointers with gap
```

---

# 24. Tree Signals

If the input is a tree, immediately ask:

```text
Do I need:
    DFS?
    BFS?
    Recursion?
    Level order?
    Path information?
    Subtree information?
```

### DFS

Usually:

```text
depth
path
subtree
recursive relationship
```

### BFS

Usually:

```text
level
minimum number of edges
shortest path in unweighted tree
```

---

# 25. Graph Signals

Look for:

```text
cities
roads
connections
network
dependencies
relationships
routes
reachability
```

Translate:

```text
Objects → Nodes

Relationships → Edges
```

Then ask:

```text
Directed or undirected?

Weighted or unweighted?

Need traversal?

Need shortest path?

Need connectivity?

Need ordering?
```

---

# 26. Graph Algorithm Recognition

| Problem Property                | Algorithm              |
| ------------------------------- | ---------------------- |
| Traverse graph                  | DFS / BFS              |
| Connected components            | DFS / BFS / DSU        |
| Shortest path, unweighted       | BFS                    |
| Shortest path, positive weights | Dijkstra               |
| Negative edges                  | Bellman-Ford           |
| Minimum spanning tree           | Kruskal / Prim         |
| Dependency ordering             | Topological Sort       |
| Detect cycle, undirected        | DFS / DSU              |
| Detect cycle, directed          | DFS / Topological Sort |

---

# 27. Backtracking Signals

Think Backtracking when the problem asks for:

```text
all combinations
all permutations
all subsets
all valid arrangements
generate
choose / don't choose
```

Typical structure:

```text
Choose
 ↓
Explore
 ↓
Undo
```

Example:

```text
Subsets
```

At every element:

```text
Take it
OR
Don't take it
```

This creates a decision tree:

```text
             []
           /    \
        [1]      []
       /  \      / \
    [1,2] [1]  [2] []
```

---

# 28. Dynamic Programming Signals

DP is often overused.

Do not think:

> "The problem is difficult, so it must be DP."

Look for these two properties:

## 1. Overlapping Subproblems

The same subproblem is solved repeatedly.

## 2. Optimal Substructure

The optimal solution can be constructed from optimal solutions to smaller subproblems.

Typical signals:

```text
maximum
minimum
number of ways
count ways
can we
best possible
longest
shortest
choose / skip
```

But these words alone do not prove DP.

---

# 29. DP Recognition Framework

Ask:

```text
Can I define a smaller state?

        ↓

Does solving the smaller state help solve the larger state?

        ↓

Are the same smaller states repeated?

        ↓

Can I define:

dp[state] = answer for that state?
```

Then determine:

```text
State
Transition
Base Case
Order of Computation
```

---

# 30. Common DP State Patterns

### 1D DP

```text
dp[i]
```

Usually:

```text
answer up to i
```

Examples:

```text
Climbing Stairs
House Robber
Maximum Subarray variants
```

---

### 2D DP

```text
dp[i][j]
```

Usually:

```text
first i elements
+
first j elements
```

Examples:

```text
LCS
Edit Distance
Knapsack
```

---

### Grid DP

```text
dp[row][col]
```

Examples:

```text
Unique Paths
Minimum Path Sum
```

---

### Knapsack Pattern

Ask:

```text
For each item:

Take it?
Don't take it?
```

This is a huge DP signal.

---

# 31. Bit Manipulation Signals

Look for:

```text
XOR
bits
binary
odd/even
power of 2
single number
toggle
mask
subset
```

Important identities:

```text
x ^ x = 0

x ^ 0 = x

x & (x - 1)
```

The expression:

```text
x & (x - 1)
```

removes the lowest set bit.

Useful for:

```text
counting bits
checking powers of two
bit manipulation
```

---

# 32. Sorting as a Pattern

Sorting is not merely an algorithm.

It is often a **preprocessing technique**.

Ask:

> Would sorting reveal an ordering that makes the problem easier?

Examples:

```text
Two Sum
Intervals
Meeting Rooms
3Sum
Greedy problems
Duplicate detection
Closest elements
```

Often:

```text
Unstructured input
        ↓
Sort
        ↓
Two Pointers / Greedy / Binary Search
```

---

# 33. Data Structure Selection Framework

Instead of memorizing:

```text
HashMap → Two Sum
```

memorize the underlying requirement.

| Requirement             | Data Structure                      |
| ----------------------- | ----------------------------------- |
| Fast lookup             | HashMap / HashSet                   |
| Ordered lookup          | TreeMap / BST                       |
| Min / Max repeatedly    | Heap                                |
| LIFO                    | Stack                               |
| FIFO                    | Queue                               |
| Priority processing     | Heap                                |
| Prefix/range queries    | Prefix Sum / Fenwick / Segment Tree |
| Connectivity            | DSU                                 |
| Hierarchical data       | Tree                                |
| Relationships           | Graph                               |
| Frequency               | HashMap / Array                     |
| Nearest greater/smaller | Monotonic Stack                     |

---

# 34. Algorithm + Data Structure Combinations

Real interview problems frequently require a combination.

Examples:

```text
Sliding Window + HashMap

Prefix Sum + HashMap

Binary Search + Greedy

Sorting + Two Pointers

Heap + HashMap

DFS + HashSet

BFS + Queue

Graph + Topological Sort

DP + HashMap

Monotonic Stack + Array
```

This is a much better mental model than trying to classify every problem into exactly one algorithm.

---

# 35. The 10 Questions You Should Ask for EVERY Problem

Before coding, answer these:

```text
1. What exactly is the problem asking?

2. What are the inputs and outputs?

3. What are the constraints?

4. Is order important?

5. Is the problem about contiguous elements?

6. What operation is repeatedly required?

7. What information do I need to remember while processing?

8. Can I eliminate repeated work?

9. What is the simplest brute-force solution?

10. Why is the optimized solution better than brute force?
```

If you cannot answer these, you are not ready to code.

---

# 36. The Brute Force → Optimization Method

Do NOT immediately search for the optimal algorithm.

First derive brute force.

Example:

```text
Find maximum sum subarray.
```

Brute force:

```text
for i
    for j
        calculate sum
```

Complexity:

```text
O(N³)
```

Improve:

```text
Reuse previous sum
```

Now:

```text
O(N²)
```

Then observe:

```text
Can the maximum be maintained while traversing?
```

This leads to:

```text
Kadane's Algorithm
O(N)
```

This process develops problem-solving ability.

---

# 37. The "Repeated Work" Question

One of the most powerful questions in DSA is:

> What work am I doing repeatedly?

Example:

```text
Find sum of every subarray.
```

Naive:

```text
Calculate each sum from scratch.
```

Repeated work:

```text
Same elements are added again and again.
```

Optimization:

```text
Prefix Sum
```

---

Another example:

```text
Find whether an element appeared before.
```

Naive:

```text
Search previous elements every time.
```

Repeated work:

```text
Repeated lookup.
```

Optimization:

```text
HashSet
```

---

Another:

```text
Find next greater element.
```

Naive:

```text
Scan right for every element.
```

Repeated work:

```text
Elements are repeatedly compared.
```

Optimization:

```text
Monotonic Stack
```

---

# 38. The "What Must I Remember?" Question

This is another extremely powerful technique.

Ask:

> While scanning the input, what information do I need to remember?

Examples:

### Need frequency

```text
HashMap
```

### Need whether something exists

```text
HashSet
```

### Need minimum / maximum

```text
Heap
```

### Need previous unresolved elements

```text
Stack
```

### Need current range

```text
Sliding Window
```

### Need cumulative information

```text
Prefix Sum
```

### Need connectivity

```text
DSU
```

### Need state of previous decisions

```text
DP
```

---

# 39. Pattern Recognition Cheat Sheet

| Signal                   | Think                        |
| ------------------------ | ---------------------------- |
| Contiguous               | Sliding Window / Prefix Sum  |
| Subarray                 | Sliding Window / Prefix Sum  |
| Substring                | Sliding Window               |
| Sorted                   | Binary Search / Two Pointers |
| Pair                     | HashMap / Two Pointers       |
| Triplet                  | Sorting + Two Pointers       |
| Frequency                | HashMap                      |
| Duplicate                | HashSet                      |
| Top K                    | Heap                         |
| Kth largest              | Heap / Quickselect           |
| Next greater             | Monotonic Stack              |
| Previous smaller         | Monotonic Stack              |
| Parentheses              | Stack                        |
| Interval                 | Sort + Greedy / Heap         |
| Connected                | DFS / BFS / DSU              |
| Shortest unweighted path | BFS                          |
| Shortest weighted path   | Dijkstra                     |
| Dependencies             | Topological Sort             |
| All combinations         | Backtracking                 |
| All permutations         | Backtracking                 |
| Minimum / Maximum ways   | DP / Greedy                  |
| Number of ways           | DP                           |
| Choose / Skip            | DP / Backtracking            |
| Monotonic condition      | Binary Search                |
| Range sum                | Prefix Sum                   |
| Dynamic range query      | Fenwick / Segment Tree       |
| Tree levels              | BFS                          |
| Tree paths               | DFS                          |
| Linked list cycle        | Fast / Slow                  |
| Middle of linked list    | Fast / Slow                  |
| XOR                      | Bit Manipulation             |
| Power of 2               | Bit Manipulation             |
| Connectivity merging     | DSU                          |

---

# 40. A Better Problem-Solving Template

For every problem you practice, write this BEFORE coding:

```text
Problem:
________________________________

Input:
________________________________

Output:
________________________________

Constraints:
________________________________

Important Keywords:
________________________________

Is order important?
YES / NO

Contiguous?
YES / NO

Sorted?
YES / NO

Repeated operation:
________________________________

What information must I remember?
________________________________

Brute Force:
________________________________

Brute Force Complexity:
________________________________

Why is brute force too slow?
________________________________

Possible Pattern:
________________________________

Required Data Structure:
________________________________

Optimized Algorithm:
________________________________

Time Complexity:
________________________________

Space Complexity:
________________________________

Why does this work?
________________________________

Edge Cases:
________________________________
```

This template should become your standard workflow.

---

# 41. Example — Apply the Framework

Problem:

> Given an array of positive integers and an integer K, find the length of the smallest contiguous subarray whose sum is at least K.

---

## Step 1: What is being asked?

```text
Smallest length
```

Optimization problem.

---

## Step 2: Important keyword

```text
CONTIGUOUS
```

Therefore:

```text
Subarray
```

---

## Step 3: Constraint

Suppose:

```text
N <= 100,000
```

Therefore:

```text
O(N²)
```

is probably too slow.

---

## Step 4: What operation?

Need:

```text
Subarray sum >= K
```

---

## Step 5: Important property

Array contains:

```text
POSITIVE INTEGERS
```

This is extremely important.

When we expand the window:

```text
sum increases
```

When we shrink:

```text
sum decreases
```

Therefore we can maintain a valid window.

---

## Step 6: Pattern

```text
Contiguous
+
Minimum length
+
Positive numbers
+
Maintainable window condition

        ↓

Sliding Window
```

---

## Step 7: Data Structure

We only need:

```text
left
right
currentSum
```

No HashMap required.

---

## Step 8: Complexity

```text
Each element enters the window once.
Each element leaves the window once.

Time: O(N)
Space: O(1)
```

This is pattern recognition.

---

# 42. Example — Same Topic, Different Pattern

Problem:

> Given an array containing positive and negative integers, find the number of subarrays whose sum equals K.

Signals:

```text
Subarray
+
Sum
+
Count
+
Negative numbers possible
```

Can we use ordinary Sliding Window?

No.

Why?

Because with negative numbers:

```text
Expanding window
```

does not necessarily increase sum.

And:

```text
Shrinking window
```

does not necessarily decrease sum.

Therefore the monotonic property required by ordinary Sliding Window is missing.

Instead:

```text
Prefix Sum
+
HashMap
```

This is an extremely important interview lesson:

> Similar-looking problems can require completely different patterns because one property changes.

---

# 43. Pattern Confusion: Sliding Window vs Prefix Sum

Use this rule:

### Sliding Window

Works especially well when the window condition is **monotonic** as the window expands/shrinks.

Example:

```text
Positive numbers
sum >= K
```

---

### Prefix Sum

Useful when you need:

```text
exact range sums
subarray sum = K
count subarrays by sum
```

Especially when:

```text
negative numbers exist
```

---

# 44. Pattern Confusion: HashMap vs Sorting

Problem:

```text
Find duplicates.
```

Possible:

```text
HashSet → O(N) average
```

or:

```text
Sort → O(N log N)
```

How do you choose?

Ask:

```text
Do I need original order?

Do I have memory restrictions?

Do I need ordered information later?

Is O(N) expected?

Can modifying the array be allowed?
```

The correct data structure depends on the full problem, not just the first sentence.

---

# 45. Pattern Confusion: DFS vs BFS

Ask:

### Do I care about levels / minimum number of steps?

```text
YES → BFS
```

### Do I care about exploring paths / subtree structure?

```text
YES → DFS
```

Example:

```text
Minimum number of moves in an unweighted graph
```

→ BFS

Whereas:

```text
Detect connected components
```

→ DFS/BFS both work.

---

# 46. Pattern Confusion: Greedy vs DP

Ask:

> Can I make a local decision and permanently discard the alternatives?

If yes, Greedy may work.

But you need proof.

If:

```text
Current decision affects future possibilities
```

and multiple states must be considered:

```text
DP
```

A common mistake is assuming:

```text
"maximum/minimum" = DP
```

This is false.

---

# 47. Pattern Confusion: Backtracking vs DP

Both may explore choices.

Difference:

### Backtracking

You want:

```text
ALL valid solutions
```

Example:

```text
Generate all subsets.
```

---

### DP

You want:

```text
BEST / COUNT / POSSIBLE
```

and subproblems overlap.

Example:

```text
Maximum profit
Number of ways
Can target be formed?
```

---

# 48. The Interview Decision Tree

Use this mental flow:

```text
                    START
                      |
                      v
               What is the input?
                      |
       +--------------+--------------+
       |              |              |
     Array          String          Graph
       |              |              |
       v              v              v
 Contiguous?      Substring?     Connected?
       |              |              |
      YES            YES            YES
       |              |              |
 Sliding Window   Sliding Window  DFS/BFS/DSU
       |
      NO
       |
       v
    Sorted?
       |
   +---+---+
   |       |
  YES      NO
   |       |
Two Ptr  HashMap?
Binary     |
Search     |
           v
       Frequency?
           |
          YES
           |
        HashMap
```

This is not a rigid decision tree.

It is a **thinking aid**.

---

# 49. The Three-Layer Model

When solving any problem, think in three layers.

## Layer 1 — Problem Structure

```text
Array?
String?
Tree?
Graph?
Intervals?
Matrix?
```

---

## Layer 2 — Required Operation

```text
Search?
Count?
Minimize?
Maximize?
Find nearest?
Traverse?
Generate?
Connect?
```

---

## Layer 3 — Optimization Technique

```text
Hashing
Sorting
Two Pointers
Sliding Window
Binary Search
Heap
Stack
Prefix Sum
Greedy
DP
Graph Algorithms
Backtracking
```

Example:

```text
Array
  ↓
Contiguous range
  ↓
Longest valid range
  ↓
Sliding Window
```

Another:

```text
Array
  ↓
Frequency
  ↓
Fast lookup
  ↓
HashMap
```

Another:

```text
Array
  ↓
Nearest greater
  ↓
Previous unresolved elements
  ↓
Monotonic Stack
```

---

# 50. Don't Memorize Problems — Memorize Transformations

Instead of remembering:

```text
Two Sum → HashMap
```

remember:

```text
Need complement lookup
        ↓
HashMap
```

Instead of:

```text
Longest Substring Without Repeating Characters
        ↓
Sliding Window
```

remember:

```text
Longest contiguous range
+
Maintain validity
        ↓
Sliding Window
```

Instead of:

```text
Daily Temperatures
        ↓
Monotonic Stack
```

remember:

```text
Next greater element
        ↓
Monotonic Stack
```

This makes the knowledge transferable.

---

# 51. Your DSA Pattern Notebook

For every pattern, maintain four things:

```text
1. Recognition Signals

2. Core Invariant

3. Generic Template

4. Problems
```

Example:

## Sliding Window

### Recognition Signals

```text
Substring
Subarray
Contiguous
Longest
Shortest
At most K
At least K
```

### Core Invariant

```text
Current window satisfies a condition.
```

### Template

```text
left = 0

for right := 0; right < n; right++ {

    add(arr[right])

    for window invalid {
        remove(arr[left])
        left++
    }

    update answer
}
```

### Problems

```text
Longest Substring Without Repeating Characters
Minimum Size Subarray Sum
Longest Repeating Character Replacement
Minimum Window Substring
```

---

# 52. The "Invariant" Is the Secret

For senior-level interviews, don't just know the code.

Know the invariant.

Example:

### Sliding Window

Invariant:

```text
The current window [left, right]
satisfies the required constraint.
```

---

### Binary Search

Invariant:

```text
The answer always remains inside [low, high].
```

---

### Heap

Invariant:

```text
Heap root contains the currently required
minimum/maximum candidate.
```

---

### BFS

Invariant:

```text
Nodes are processed in non-decreasing distance
from the source in an unweighted graph.
```

---

### DFS

Invariant:

```text
All reachable nodes from the current state
are explored according to the traversal.
```

---

### DP

Invariant:

```text
dp[state] represents a precisely defined
subproblem answer.
```

If you understand the invariant, the implementation becomes much easier.

---

# 53. How to Practice Pattern Recognition

Do NOT solve 100 random problems.

Instead use:

```text
Pattern
    ↓
Easy Problem
    ↓
Medium Problem
    ↓
Medium Variant
    ↓
Hard Variant
```

For example:

```text
Sliding Window

1. Maximum sum subarray of fixed size
2. Longest substring without repeating characters
3. Minimum Size Subarray Sum
4. Longest Repeating Character Replacement
5. Minimum Window Substring
```

The goal is to see how the same pattern evolves.

---

# 54. The "Why Not?" Technique

After solving a problem, ask:

```text
Why not brute force?

Why not HashMap?

Why not Sliding Window?

Why not Sorting?

Why not Binary Search?

Why not DP?

Why not Greedy?
```

This develops algorithm discrimination.

Example:

```text
Why not Sliding Window?

Because negative numbers destroy
the monotonic sum property.
```

That explanation is much more valuable than simply memorizing:

```text
"Use Prefix Sum + HashMap."
```

---

# 55. Your 5-Minute Pre-Coding Routine

Before writing code, spend approximately five minutes:

```text
Minute 1
--------
Understand the problem.

Minute 2
--------
Extract constraints and identify the input structure.

Minute 3
--------
Derive brute force.

Minute 4
--------
Find repeated work / important property.

Minute 5
--------
Select pattern + data structure + complexity.
```

Only then start coding.

---

# 56. A Stronger Interview Workflow

During an interview, communicate your thinking:

```text
"Let me first clarify the constraints."

"The important property here is that the array
contains only positive numbers."

"Since the problem asks for a contiguous range,
I am considering a sliding-window approach."

"The positive-number constraint gives us the
monotonicity required to shrink the window safely."

"The brute-force solution would be O(N²),
but we can reduce this to O(N)."

"I'll maintain the invariant that the current
window satisfies the required condition."
```

This demonstrates senior-level problem solving.

---

# 57. Pattern Recognition Master Checklist

Before looking at the solution, ask:

```text
[ ] What is the input structure?

[ ] What exactly is the output?

[ ] What are the constraints?

[ ] Is the input sorted?

[ ] Does order matter?

[ ] Is it contiguous?

[ ] Is it a subarray or subsequence?

[ ] Is it asking for frequency?

[ ] Is fast lookup required?

[ ] Is it asking for nearest greater/smaller?

[ ] Is it asking for Top K?

[ ] Is it asking for minimum/maximum?

[ ] Is there a monotonic property?

[ ] Is there a repeated subproblem?

[ ] Are there choices to enumerate?

[ ] Is it a graph?

[ ] Is it a dependency problem?

[ ] Can sorting simplify the problem?

[ ] What is the brute-force solution?

[ ] What work is repeated?

[ ] What information must I remember?

[ ] What invariant can I maintain?

[ ] What is the expected complexity?
```

---

# 58. The Ultimate Mental Model

Whenever you encounter a new DSA problem:

```text
                    PROBLEM
                       |
                       v
                Understand it
                       |
                       v
                  Constraints
                       |
                       v
                Input Structure
                       |
                       v
                Required Output
                       |
                       v
               Required Operation
                       |
                       v
              Important Properties
                       |
                       v
                Brute Force
                       |
                       v
              Repeated Work?
                       |
                       v
               Optimization
                       |
                       v
                 PATTERN
                       |
                       v
               DATA STRUCTURE
                       |
                       v
                 ALGORITHM
                       |
                       v
                INVARIANT
                       |
                       v
                 COMPLEXITY
                       |
                       v
                   CODE
```

The most important transition is:

```text
Problem
   ↓
Properties
   ↓
Pattern
```

Not:

```text
Problem
   ↓
Remembered Solution
```

---

# 59. Final Rule

When you get stuck on a DSA problem, do not immediately look at the solution.

Instead write:

```text
1. What is the brute force?

2. Why is it too slow?

3. What work is repeated?

4. What property have I not used yet?

5. What information do I need to remember?

6. Can sorting help?

7. Can hashing help?

8. Can two pointers help?

9. Can I maintain a window?

10. Is there a monotonic property?

11. Is there a smaller state?

12. Can I represent the problem as a graph?

13. Am I trying to find all possibilities?

14. What invariant can I maintain?
```

If you consistently follow this process, your objective should eventually become:

> **I don't need to remember the solution. I need to recognize the structure that forces the solution.**

That is the core DSA skill.
