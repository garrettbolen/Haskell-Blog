# Entry 6: Recursion
In this blog entry I would like to discuss the importance of recursion, especially within the context of functional programming. To many, recursion may seem like a daunting thing, but with a little practice and taking it step by step you might realize that it isn't so bad. Whether you realize it or not, recursion is all around us. From the moment we began to count we practiced a form of recursion through inductive reasoning. We started with learning the number one, then two, then three and so on. Each successive number building from the last is in and of itself a recursive process. I would like to share with you a couple classic examples of problems that can easily be solved with a few lines of recursive code.

### Problem 1
*Write a recursive function that given an input n sums all nonnegative integers up to n. For example, sum(4) -> (1+2+3+4) -> 10.*

The nature of recursion is to take a problem and reduce it into a simpler form that can be more easily computed. We must ask ourselves what the simplest possible input is for the function, otherwise known as a base case. For this problem, our base case is `sum(0) -> 0`. The next step in the problem is to write down several examples of cases that follow the base case. Let's see how the function would look for `n=1...4`.
```
sum(1) -> 1
sum(2)-> 1+2
sum(3) -> 1+2+3
sum(4) -> 1+2+3+4
```
The next step in solving the problem is to analyze the examples and try to find a pattern. You may notice that for each value of `n`, `sum(n) = (sum(n-1)) + n)`. If we combine this with our base case, we can write a function in Haskell like so:
```
sum :: Int -> Int
sum 0 = 0
sum n = n + sum (n-1)
```
With this function, each value of `sum n` all the way down to zero will be evaluated and then added together to produce an answer.

### Problem 2
*Write a function that takes two inputs n and m and outputs the number of unique paths from the top left corner to the bottom right corner of an n x m grid. Constraints: you can only move down or right 1 unit at a time.*

While this problem is a bit more challenging than the last, it is manageable if we break it down into parts (as are most recursive problems). The first step we should take is to make note of the simplest possible input (or inputs). Listing a few examples, a pattern emerges:
```
paths(1,1) -> 1
paths(2,1) -> 1
paths(1,2) -> 1
paths(1, m) -> 1
paths(n, 1) -> 1
```
It is clear that if one dimension of the grid is equal to one then there is only one possible path. With this knowledge we can formulate a concise base case that states:
`paths(n, m) -> 1 if n = 1 or m = 1`.
Here is a visualization of more potential cases:
![Grids](https://imgur.com/a/KNXwQ5h)
Notice that the total number of paths of the 3x3 grid can be found by adding the number of 2x3 paths to the number of 3x2 paths. You will find that this pattern holds true for larger grids as well. We can generalize this pattern like so:
`paths(n, m) -> paths(n, m - 1) + paths(n - 1, m)`
If we combine the base case and pattern we can write the code in Haskell:
```
paths :: Int -> Int -> Int
paths n 1 = 1
paths 1 m = 1
paths n m = paths n (m - 1) + paths (n - 1) m
```
While recursive problems may seem difficult to wrap your head around at first, it's remarkable how elegant and simplistic their solutions end up being. Oftentimes the most complex of problems will have recursive solutions of only a few lines of code.
