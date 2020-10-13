# The basics of Haskell
In this tutorial I will be covering the basics of Haskell. To start I would like to give a run down on basic info regarding the language:
1. Haskell is statically typed. All types are checked at compile-time and programs with type errors will not compile.
2. Haskell is a functional programming language. What this entails was covered in the last blog entry.
3. Haskell is "pure", meaning no data types are mutable, calling the same function with the same arguments will return the same result every time, etc.

### Declaring variables
In this code block, the declaration of variables in Haskell is demonstrated:
```
--A simple declaration of x
x :: Int 
x = 5
```
Note the syntax used in this program. `--` is used to indicate the start of a comment. `::` can be read as "has type", meaning x is of the type Int. The actual defining of x is simple, using an `=` sign like in most other languages. Note that in other languages, `=` indicates the assignment of some value to a variable, where in Haskell it quite literally defines that variable as that value (remember variables are immutable).
### Data types
The data types in Haskell are the same as in other languages. Integers, Booleans, doubles, floats, strings, and characters all exist within the language the same as any other.
### GHCi
As covered before, GHCi is the interactive Haskell shell provided with GHC. Some useful commands include:
```
:load
:type
:help
```
Load is used to compile files and can be executed with `:l`. Type returns the data type of a variable passed into it and can be executed with `:t`. Help gives the full list of functions and can be executed with `:?`.
### Function definitions
As Haskell is a functional programming language, the definition of functions is relatively simple. The best way to learn is to see an example and explain it after. For this we can look at the function we wrote earlier:
```
factorial :: Int -> Int
factorial 0 = 1
factorial n = n * factorial (n - 1)
```
The first line of this program denotes what type of input and output the function has. For this, `::` is used to denote "is of type" and `->` is used to separate the input (left) from the output (right). As shown, this function takes an integer as an input and returns an integer as well. The next two lines show different behaviors of the function. We explicitly define the input of 0 to return 1, but if it is anything other than 0 we make a recursive call on the function.
