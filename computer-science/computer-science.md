# Computer Science

Closed under: make an array of arrays, make a cons of cons. Not closed cant make array of arrays

Referential transparency - does not have internal hidden dependencies that would change the result of a call with the same args
referential transparent stuff can be memoized

idempotence: repeatable without changing state after the first call

dynamic programming: divide and conquer with memoization/caching


Verification is one aspect of testing a product's fitness for purpose. Validation is the complementary aspect.

    Validation: "Are we trying to make the right thing?", i.e., is the product specified to the user's actual needs?
    Verification: "Have we made what we were trying to make?", i.e., does the product conform to the specifications?


An impure function is one whose output depends on something other than the arguments, The output depends on something that is not an input

memoization - cache the result of func calls

tail call optimization

a calculus is a system

code is data

higher order functions do at least one of the following
accept a function as a parameter
return another function
functions can be passed around
pass a function around

take a block return a block

type erasure: annotations/type info removed during compilt time, assembly does not have types

turing machines vs lambda calculus ( shown to be of similar power )

von neuman architechture ( real world implementation of turing machine )

functional programing is a practical implementation of lamba calculus

all variables are final( they are not really variables ) -> they are symbols
all values are symbols

fp was designed/focused for calculations
keep state over time using the stack ( recursive calls )
tail call optimization: turn recursive into interative


No side effects:
no side effects -> the only effect of evaluating a function is its return value and the only thing that affects the return value of a function is its arguments.
because of no side effects the program does not have to be executed sequentially
no side effect benefits:
unit testing. dont need to worry about the state being changed by the function.
no side errects means debugging is simple
concurrency: fp programs are trivally paralizable
Hot code deployments - dont have to stop and restart the systems
machine assited proofs




Currying:
wrapping a function
int pow(int i, int j);
int square(int i)
{
    return pow(i, 2);
}
transforming functions of multiple args into a series of single calls, not just fixing the value of one arg.
a function of n variables into functions of single args.


Lazy Evaluation
infinite data structures(pi calculator)
the disadvantage is using IO and native functions(syscalls), worked around by continutations, monads, and uniqueness typing


Continuations
tell a function where to return, slightly different than blocks
no need for a stack frame
it is the passed coninuation that returns a value to where the original function is called


Pattern Matching
allow for multiple function definitions of the same function with different args and the compiler matches the calls
int fib(0) {
    return 1;
}
int fib(1) {
    return 1;
}
int fib(int n) {
    return fib(n - 2) + fib(n - 1);
}

or

int f(int n < 10) { ... }
int f(int n) { ... }
is more complex pattern matching, it is basically the compiler handling branching(conditional statements)


Closures
reference code in enclosing scope


Data dependence
true - read after write
antidep - write after read
  (storage related)
output - write after write
  (storage related)
input - read after read
