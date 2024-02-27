Data is info, plus operation it is the base of everything. 

Data (has) type 
Very basic, like a unit, mainly depends on way of storing, it makes an information settled down in physical storage. 
 (in Java primitive = direct, reference = index) >>> possible operation

Why? cuz a unit of data has to be presented in one way or another. 

Data Structure 
What does data structure depend on: 
relationships between data units, so when a group of data is organised in (some) same way in the memory (not how a single is settled down but relations in a group)
Data units >>>data structure
>>> different way of access and adjustment

Data structure >>> Decoupling >>> manipulated by the idea of ABSTRACTION >>> Abstract data type 
OPERATIONS >>> Decoupling >>> Designed Interfaces

Why? usage from the point of view of the user is better, you can ignore a lot of inner complications(such as choices of algorithms and data structure) 
Simple categorisation: Creator, producer, observer, mutator
ADT provides interface >>> And the users do implementation 

What possible functions we want to achieve:
Collections
Storage and retrieval
Sorting
Searching
>>> Algorithms

1. Storage and organisation pattern > DESIGN PATTERN
2. Basic Operations 
- (implementation for ADT)
- declaration and intialisation
JL04-Factories	
ABSTRACTION on CREATIONAL PROCESS 
Material (parameter) > Factory(Hide nearly every implementation) > Product
 

- access
access ADT
(get() is not enough) > JL13-Iterators 
The traversal of collection of data using a standard interface without knowing the details of internal data structure > Independence 
Java.util.Iterator Operation:
hasNext: start and end 
Basically a current element + a pointer
Next: return current and move on
Remove = last return by next
: need implementation, default will return unsupportedoperation
Iterator >> Iterable Collection (ADT thoughts of hidden implementation) 

Iterator + Insertion/Removal + Iterator = original Iterator ？
Depend on implementation of iterator
During: CurrentModificationException > util.ListIterator (for Object): both way iterator pre/next > add before the iterator pointer, set must be after .next

TreeIterator:
Stack - DFS 左node pop push.element完 中.. 右..

API decisions: 
?Allow modification
?NewFutureItem
?NewPastItem

- Compare values
怎么体现unit Order: java.lang.comparable > Comparable Elements / (Comparator)
很多operation的本质就是比较
- add/remove elements
- change order
- target search/retrieval 
* Advantage and disadvantage analysis facing different problems
- Collective Operations 
JL03-Collections 
List - ArrayList and LinkedList 
3. Java language traits


JL01-(Unsorted) Arrays
JL05-SortedArrays 
Array is a sequence of indexed elements and its length is fixed.  

That’s why Arrays are objects and reference type, array is not special except their “class” is an unchangeable setting in java language

Array.length 是 index

Why arrayLIst is better than array and why array is better than arrayList 

Array equality
比较的是引用对象还是具体内容 - method 不一样 注意嵌套 注意重写的到底是针对谁的
2D array  { {}  {} }
deepEqual 一样的问题

Two Implementation with same ADT array:
Unsorted array and sorted array (specific order) 

in sorted array all build on Comparable element 
Binary Search (recursion and iteration) 
contains/elementAt/remove/add/removeAll 

The interface provides operation such as:
Size (Insertion) Add/Remove (Search) Contain/ElementAt

Unsorted array >>> Sorted array Complexity Change 
contains (linear > log)
remove (constant > linear)
add (constant > linear)
*Insertion & Search Trade-off

JL06-LinkedLists 
JL10-DoublyLinkedLists

可以发展为ADT

more flexible in someway 
Have to go through one by one from root, no index

Operation:
Insert/Remove
- Head insertion (before.next = nn.next; before.next = nn;)
- Tail insertion (before.next = nn; nn.next = after;)
The insert and remove of a node is based on its relation with other nodes.
Head (can be a fake one) -  (predecessor - antecedents) - tail
Search & Get Element >>> contains/elementAt
Traverse

Tail node = null;

Sorted array >>> SIngleLinkedList Complexity Change 
remove (linear > linear)
add/insertion (linear > constant)
Based on known info: index/element/predecessor/root
contains (log > linear)
ElementAt (constant > linear) 
Size: constant or linear based on current_size variable availability
More COSTLY on space 
(LIST Interface >>>ArrayList = dynamic array: *Insertion & Search Trade-off)

> Collection  

SingleLinked >>> DoubleLinked

Known info: index/element/predecessor/antecedent/root

SingleLinked >>> DoubleLinked Complexity Change 
remove (linear > constant): in singleLinked we have .next but not .previous so we have to iterate to find the predecessor to unlink the predecessor.next
More COSTLY on space(for constant operation)

Circulation = no head and no tail 

JL07-Stacks 
JL08-Queues	

THEY ARE FAMOUS ABSTRACT DATA TYPES
How ADT choose the implementation data structure：
SLL

Head
Tail
Add
O(1)
O(1)
Remove
O(1)
O(n)
DLL

Head
Tail
Add
O(1)
O(1)
Remove
O(1)
O(1)
Array/ArrayList

Head
Tail
Add
O(n)
O(1)*
Remove
O(n)
O(1)

Stack can be implemented by unsorted array, linked list and arrayList
Stack is a container of objects following LIFO principle. 
Best Space: unsorted array
Dynamic size: Lists
Expansion Simplicity: Linked List  
Operation complexity: similar

Complexity e.g. LinkedList 
ALL constant
clear() is constant by Stack emptystack = new Stack

Application
- Reverse sth
- RPN 
- Program execution management (先放在其他地方处理完小任务再return回来）
- Web History

Queue can be implemented by unsorted array, linked list and arrayList
Queue is a container of objects following FIFO principle. 
Best Space: unsorted array
(Circular:
 FIFO is maintained by the update of front and rear.
Use % [ ].length to use the dequeued front space in array)

Dynamic size: Lists
Expansion and contraction Simplicity: Linked List 
Front = back 
(Steady point of head and tail >>> not like array where back = front + current_size) 
*Space Efficiency = CircularListQueue: back.next = front (no variable for front actually, just like before there’s no back variable) 
Enqueue:Here we use rear.next = nn.next （某种意义上的头插法)
Dequeue: rear.next = rear.next.next 
rear.next = rear

Operation complexity: similar

Complexity 
ALL constant
clear() is constant by Queue emptyqueue = new Queue

Application
- Producer and Consumer problem > enqueue dequeue achieves decoupling
- CPU ready_queue 等待执行任务管理

JL11-Trees 
Generalisation of Linked List
Specialisation of graph
Good for hierarchical data
Root node - interior node - leaf node/terminal
(Parent - child) > subTree
Depth/level index starts from 0
>>BinaryTree
 Left < element < Right
Add:go down recursively
Remove: reconstruct the subtree by add to achieve balance
Size(number of node): recursive
Complexity: all linear
Application:
Search Tree - file system
Heaps 
Traversal
Depth First: recursive / stack : stack [ ] visit [ ]
- Preorder - linear ordering 
Root开始包围回到root

- Postorder - for node v and v’ ’s child
走完child走parent
- Inorder - 
左扫描到右
Express Notations correspond to:
Prefix: PN operator+operands
Infix: normal+brackets for subtree
Postfix:RPN like stack operands + operator
Breath First: queue
level down

RHWeek8 Hash Map and hash table
Insertion
Removal
isEmpty
Find
Size
Keys
Values


RHWeek10 graph  
Network = Graph = Collection of nodes + edges
- labelled
- weighted
- directed
Degree = number of edges for a node > in-degree/out-degree
Node - edge - node = adjacent
Neighbour - neighbourhood
Path.length = node number - 1
 - Unravel a graph to a tree > trees are acyclic
Subgraph
- connected > connected subgraph = connected components
Graph Interface
addNode()
removeNode(v)
addEdge(v1, v2)
removeEdge(v1, v2)
setLabel(v_or_e)
getLabel(v_or_e)
degree(v)
endpoints(e)
traverse(e, v)
areAdjacent(v1, v2)
neighbours(v)
nodes()
edges()
Global and local operations 

Ways of implementation:
- EdgeList+NodeList = O |E|
> global to local edge list
- AdjacencyList = O (k) > O (mn) > O (n^3)
TimeConsuming
- AdjacencyMatrix
SpaceConsuming/Moderation
