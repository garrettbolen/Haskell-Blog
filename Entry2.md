# Entry 2: Functional programming
In this entry, we will be covering the basics of functional programming and some of its many advantages. First, I would like to discuss the difference between imperative and functional programming languages.
### Imperative programming languages
Imperative programming languages use sequences of statements that determine how to reach an end goal. As each statement is executed, the state of the program changes with it. For example, in a language like C++, which is imperative, you may find a program such as:
```
int i = 2;
int j = 3;
int sum = i + j;
```
In this program, the state of the program is altered with each assignment of a new variable. In imperative programming languages, explicit instructions are given to a computer for it to execute.
### Functional programming languages
Where imperative programming relies on giving sequential instructions to the computer to execute, functional programming lays out a blueprint for what things are and how they should behave. One of the most common "Hello World" type programs in recursive programming is the factorial function. In Haskell, a functional programming language, it can be written: 
```
factorial 0 = 1
factorial n = n * factorial (n - 1)
```
In functional programming, the logic of computation is defined with little emphasis on the order of execution. This is demonstrated through this recursive program nicely because there are no explicit directions for which to execute first. There are simply two cases defined and upon a function call whichever one fits the case will be executed.
### Advantages of functional programming languages
One of the main advantages of functional programming is the ability for functions to be self-contained. That is, if you go in and add new functions later or alter some aspect of the program, the previous functions you wrote will not be affected as they do not rely on any outside factors. Another benefit is increased readability and maintainability. Since functions do not rely on one another, you can go in and change whatever you like with relative ease.
