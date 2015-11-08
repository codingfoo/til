# sicp

A process is the entity in the machine, a program manipulates a process


primitive expressions - the smallest atomic unit of a program
means of combination - how to join primitive expressions
means of abstraction - naming combinations and manipulating them

operators are functions and can be returned as well as data


hash table is sorta of a table
global environment table
local environment table

learning - start with simple incomplete model and build up
use the simplest model that works

normal order vs applicative order evaluation
lisps can switch between those two models,
application aka function/procedure method call.
eval and apply : apply in this case is the calling of primitive expressions

binary search in debugging


procedures are rules for manipulating data
manipulating the list of rules(procedure, method, function) as units
anonymous data anonymous procudures
naming data and procudures

master software engineers have confidence in their software that it will do what it was written to do

figure out what the software should do(requirements) getting the software to meet the requirements


there is a difference between computing and computer science

computer science < computation

geometry = what is true, study of declarative knowledge

"computer science" = how to
"computer science" = study of imperative knowledge
"computer science/software engineering" = study of controlling complexity

The computer science complexity is different than other types of complexity because it is not real
not much difference between what I can imagine and what I can build

abstract form of engineering, ignore constraints imposed by reality

studying processes that solve problems

process: the worker, doer
procedure: pattern of rules, control the process

programming - first learning the rules and then the implications of those rules


software tests are declarative knowledge of an imperative system



## techniques to control complexity
1) black box abstraction - suppress details
  a) primitive operations
  b) combination
  c) abstraction
2) convential interfaces - agreed upon ways to connect
3) metalingustic abstraction - make a new language - create a dsl



means of combination
forming trees
naming trees

combinations can be anonymous
abstraction is separating and naming - i guess abstraction can be anonymous

anonymous closures are a litmus test for a language


no difference in primitives and what is added by the programmer

procedures without params
could be used for lazy eval
when they have side effects

wishful thinking is required as part of computer science

local names are required for black box abstraction

free vs bound variables
free = "global" or variables in scope
bound variables that are parameters

internal definitions are part of avoiding clutter in black box abstraction

procedures used as word rather than functions since functions have a mathematical derivative


rights of first class citizens in a programming language
be anonymous
to be named
pass as arguments
return as val
be part of data structures

lisp everything is an expression
what is not an expression?

code describes how a process changes over time

common patterns of usage
idioms

abstracting common patterns of usage
naming general patterns
abstracting general patterns of usage is possible when you can have higher order functions

reliably create programs that do what they are intended to do

there are differences however small in the processes of the same program run at different times or on different machines(memory layout, etc)
