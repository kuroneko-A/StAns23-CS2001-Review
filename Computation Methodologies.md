
Computation Methodologies 
The thought of programming:
JL02-TDD
Computation: 
FS
FSM: input+ history
State: inner result/current position
Finite state machine or automata are simple control systems mapping input to output with some state notions 
- collection of set
F = (S,s0,Σ,Γ,δ,ω)
All the states
A subset of state which is the initial state
Input
Output
Cartesian product of state and input > states > transition function 
Cartesian product of state and input > output > output function
- transition table 
- diagram

If δ(s,i) = δ(s′,i) and ω(s,i) = ω(s′,i) for all i ∈ I, then s and s′ are duplicate states and can be merged.

FSA is a subclass of FSM that recognise a particular sequence but not other, it does not have output functions but has accepting states
M = (A,S,F,s0,T)

Finite set of alphabet

State

Transition function 

Initial state 

Accepted states or terminals 

NFA: non-deterministic
Every NFA has a FSA

Complexity of FSA
O(n)

CFG
Grammar: a set of formal rules that defines a valid sentence would look like.
- Valid words
- Ordering
- combination

The thought of OOP: 
The god: Object
Primitive types： 复制 - 互相独立
Reference types：引用地址 - 互相影响 
Object oriented：
Object = Status + Behaviour in a memory block
variable - > domain
Field = domain
SRP
OCP
LSP
DIP
ISP
ABSTRACTION
Class
Abstract Class: class extends abstract class
Interface: class implements interface

JAVA 内存管理

This.
Throw{} and try{} catch{} Exceptions 
Final
Generic
Encapsulation
For if while

Inheritance Similarity
and 
JL14_15-Polymorphism Differences  

JL16-CollectionsFramework	 
JL17-CreatingCollections

Programming Languages or PseudoCode or Flowchart
写loop： ||/?/: operator 
