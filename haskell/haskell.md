# Haskell

ghci load file

use recursion no loops

list homogeneous

head tail of list - useful for recursion

separate pure functional core from outside world

immutable data structures

pattern matching

type inference

----

fragile functions

backticks turn any func into being used like an operator

map
filter
foldl foldr


operators on functions just like numbers

func composition
func application
func comp .

type variable -> similar to templates, related

type class constraints, so type variables can be constrained to only work on certain classes



represents code that can be run
do block
  composite io actions


functions
types
type classes
io actions


recursion and laziness allow for replacing loops with recursion without blowing stack


not keywords just functions hence lack of syntax in haskell

io actions are like registering or declaring that certain code should be run --- and then it is run

io actions and laziness are why debugging and profiling can be so weird

io actions are lazy


typeclass is a definition of a certain type and what functions have to be supported by it

a function can work with certain type classes

monads are part of the type hierarchy

in haskell a pure function is a function
a category is what we think of as functions with side effects in other langs

monads are intended to hide accidental complexity, (eg dealing with nils)




a -> (a -> b) -> b

the parens is a function


bind applies a function to a value wrapped in the monad box, leaving it in the box

do is syntactic sugar for return and bind

three penny

(foo (+)) baz      -- create a function and call with baz argument


lens library for data structure manipulation


lens

template haskell extension

prefix with underscore

make lenses


forM
replicateM
when


liftM

mapM
filterM
foldM

control.monad

unit allows for "functions" that dont return anything


procedural abstraction
