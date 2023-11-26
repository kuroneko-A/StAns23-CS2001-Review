### Data is info, plus operation it is the base of everything. 

Data (has) type 
Very basic, like a unit, mainly depends on way of storing, it makes an information settled down in physical storage. 
 (in Java primitive = direct, reference = index) >>> possible operation

Why? cuz a unit of data has to be presented in one way or another. 

Data Structure 
What does data structure depend on: 
relationships between data units, so when a group of data is organised in (some) same way in the memory (not how a single is settled down but relations in a group)
Data units >>>data structure
>>> different way of access and adjustment

Data structure OPERATIONS manipulated by the idea of ABSTRACTION >>> Abstract data type 

Why? usage from the point of view of the user is better, you can ignore a lot of inner complications(such as choices of algorithms and data structure) 
Simple categorisation: Creator, producer, observer, mutator
ADT provides interface >>> And the users do implementation 

What possible functions we want to achieve:
Collections
Storage and retrieval
Sorting
Searching

1. Storage and organisation pattern
2. Basic Operations 
- (implementation for ADT)
- declaration and intialisation
怎么体现unit Order: comparable > Comparable Elements
/ (Comparator)
很多operation的本质就是比较
- access
- Compare values
- add/remove elements
- change order
- target search/retrieval 
* Advantage and disadvantage analysis facing different problems
3. Java language traits


JL01-(Unsorted) Arrays
JL05-SortedArrays 

That’s why Arrays are objects and reference type, array is not special except their “class” is an unchangeable setting in java language

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
The insert and remove of a node is based on its relation with other nodes.
Head (can be a fake one) -  (predecessor - antecedents) - tail
Search & Get Element >>> contains/elementAt
Traverse

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
A CONTAINER OF OBJECTS: LIFO
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
A CONTAINER OF OBJECTS: FIFO
Best Space: unsorted array
Dynamic size: Lists
Expansion and contraction Simplicity: Linked List  
Operation complexity: similar

Complexity e.g. LinkedList 
ALL constant
clear() is constant by Queue emptyqueue = new Queue

Application
- Producer and Consumer problem > enqueue dequeue achieves decoupling
- CPU ready_queue 等待执行任务管理

JL11-Trees 

RHWeek8 Hash Map and hash table

RHWeek10 graph  

