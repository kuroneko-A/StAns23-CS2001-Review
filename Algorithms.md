Algorithms based on 
2 ways of solving problems 
Heuristics vs. Algorithms = Compass vs. Map = Exploration vs. A SET OF RULES
Heuristics: Some targeted input > Not guaranteed near expected => fast > may deal with infinite input > hard to replicate 
Algorithm : 
Finite input => Only result which is the expected result 
Usually guaranteed return > Termination > Predictable and trackable > and provability(?) in maths   

RHWeek5 Complexity Analysis 
4. Comparing Algorithms:
Input Characteristics
Size
Actual value > Rate (now/expected) 
Algorithms Characteristics
Algorithms analysis
> express in terms of problem size
Time: Best/Worst/Average
Space: Different Place
Better Algorithms: USE Smaller Space and Shorter Time 

Time Complexity
- define the essential operation in one step
- all operation and variables in worstCase 
The complexity of one step
How many times a step will be performed in worstCase (add up all the primitive operations) >  The theoretical running time of a algorithm
>make n infinitely large 

Size Complexity
- Consider the original input of an algorithm
- define the essential operation > memory usage in one step
- see if it uses extra memory in worstCase 
The complexity of one step
How many times in worstCase >  The theoretical memory footprint of an algorithm >make n infinitely large  

AverageCase is special

>>> Asymptotoic Analysis

we have a function s where put in the list and return the sorted
s(x)

With n being the input size of x, we have a function on n, which is f(n), express s(x) has the time complexity n^2 >> Big O Notation = Time Complexity

f(n) ∈ O(g(n))

With n being the input size of x, we have a function on n, which is f(n), express s(x) has the size complexity n >> Big Omega Notation = Size Complexity

f(n) ∈ Ω(g(n)) >> there’s a constant c such that |f(n)| ≤ c|g(n)| >> c implies upper/lower bound


- for sum > keep the overwhelming factor
- for product > keep the variable (no constant)

Order of Magnitude  
• Constant-time algorithms O(1) : independent action/hash table
• Logarithmic-time O(log(n)) : divide and conquer/binary search 
• Linear-time O(n) loop
• Linear-time O(nm) e.g. multiplication of matrix 
• Log-linear time O(n log(n)): best sorting 
• Polynomial-time O(n^c) for some constant c: loops
• Exponential time O(c^n) for some constant c : recursion/division of sub problems
• Factorial time O(n!)
https://www.bigocheatsheet.com/

>Scalability of algorithms > The growth of complexity the slower the better 

Reality: 
Size/actual value matters for large but not-infinite > constants
Space & Speed trade off e.g.
Pathological cases > Ignore, warn, change


The thought of Algorithms:
Using repetitive operation: So mostly the followings are Loop

JL09-Recursion (& Iteration) 
Something defined in terms of itself (or similar but simpler things). 
Advantages: 
- Abstraction >> Clearness and directness and easier mistake detection

rec(the updated/calculated element as parameter){
If element == xx return based_answer // one or more base case to ground recursion >> no call anymore, start to return the based_answer to the previous method
Else return onetime_answer(unit)*rec(parameter element converge) //def the return by the return of more subsequent problems
}
*Auxiliary method >>> hide other auxiliary parameters 衔接rec和大环境

Examples in both algorithms and data structure and NON-RECURSIVE data structure
One recursive call > multiple recursive call e.g. Fibonacci has (1/srt5)^n which is exponential complexity. < repeated computation of same method(para)
Optimisation:
>stackOverflow > Tail recursion: do not have to remember the result of previous call (done by a extra parameter = variable assignment) > basic a iterative > save stack spaces 
(Since java compiler does not support tail-call you have to hand write)
Memorisation: store the repeated computed resultes > linear time

RHWeek5 Sorting
In-place sorts:
Time: O(n^2)
Space:O(1)
InsertionSort
iterate through the list (starting with the second element) • at each element, shuffle the neighbors below that element up until the proper place is found for the element, and place it there.
SelectionSort
Selection Sort is another in-place sort that has a simple algorithm: • Find the smallest item in the list, and exchange it with the left-most unsorted element. • Repeat the process from the first unsorted element
BubbleSort
+ Divide and Conquer
Time: O(nlog(n))
Space:O(log(n))
- Trade off here 
MergeSort
Divide the unsorted list into n sublists, each containing 1 element (a list of 1 element is considered sorted). • Repeatedly merge sublists to produce new sorted sublists until there is only 1 sublist remaining. This will be the sorted list.
+Pivot(heuristics)
Time: O(nlog(n)) to n^2
QuickSort is inverse merge sort
Pick an element, called a pivot, from the list  Reorder the list so that all elements with values less than the pivot come before the pivot, while all elements with values greater than the pivot come after it. After this partitioning, the pivot is in its final position. This is called the partition operation. • Recursively apply the above steps to the sub-list of elements with smaller values and separately to the sub-list of elements with greater values. • The base case of the recursion is for lists of 0 or 1 elements, which do not need to be sorted.
+ in-place
Space:O(1)
CountingSort
For repeated elements

RHWeek8 BinarySearch Tree
For Sort and Search:
- dynamic data
- unbounded sizes
- T as O1 and S as Onlogn
- maintainance
**Binary Tree**
Height: longest path from root to leaves 2h+1 −1 > element > h+1
Level: x2x2x2x2
+ left node > parent > right node = invariant def
Operations:
Add
Retrieve
Delete:minimal disruption = minimal value = leftmost on the right and rightmost on the left, and treat the moved node as deletion
Correct but Imbalance > a linked list 
+ the heights of left and right children node of every node to differ at most +/- 1: balance factor = left edges - right edges
The number of element > 2^h
- maintain the log complexity

AVL Tree
Update and rebalance: label and rotate
- double rotation left right
- simple rotation left

Addition is constant
Deletion is logn

Graph Algorithms
BFS
Dijkstra’s
The weighted
