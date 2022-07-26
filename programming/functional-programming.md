# Functional Programming

Functional programming is a programming paradigm where software is built using functions that are guided by two core principles:

1. Functions are pure (no side effects)
2. Data is immutable

**Pure Functions**

Functions always give the same output for the same inputs (data in, data out). They do not include any side effects, such as logging to the console, writing to the network or modifying an external variable. They also do not call any other functions with side effects.

A significant advantage of this is that pure functions are easier to test. Input -> output, bam. No surprises.

**Immutable Data**

Data cannot be directly modified after it's created, which prevents the possibility of accidentally changing something outside of a function. In JavaScript, arrays have a number of helpful methods that embrace functional programming, such as `.map()`, `.filter()` and `.reduce()`.

**Functional Programming Languages**

Some examples of functional programming languages are:

- Clojure
- Elixir
- Elm
- Erlang
- Haskell
- OCaml

**Resources**

- [Learning Functional Programming with JavaScript](https://youtu.be/e-5obm1G_FY) by Anjana Vakil
- [What Is Functional Programming?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0) by Eric Elliott
