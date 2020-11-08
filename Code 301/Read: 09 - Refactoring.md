# Concepts of Functional Programming in Javascript

## What is functional programming?
- Functional programming is a programming paradigm 
— a style of building the structure and elements of computer programs 
— that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 
— Wikipedia

### Pure functions
- It returns the same result if given the same arguments
- If our function reads external files, it’s not a pure function — the file’s contents can change.
- Any function that relies on a random number generator cannot be pure.
- It does not cause any observable side effects

### Immutability
- When data is immutable, its state cannot change after it’s created. 
- If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

### Referential transparency
- Basically, if a function consistently yields the same result for the same input, it is referentially transparent.
- pure functions + immutable data = referential transparency

### Functions as first-class entities
- The idea of functions as first-class entities is that functions are also treated as values and used as data.
- takes one or more functions as arguments, or returns a function as its result
- Filter
- Map
- Reduce
