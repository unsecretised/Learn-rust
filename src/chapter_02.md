# Chapter 2 - Variables

Try to understand the below statement. It's ok if you don't get it, it's explained afterwards
> You set the variables mutability when you are declaring a variable

Let's unpack the above statement

A variable is used to store data.

Its concept is similar to a box (but made with glass so that you can see whats
inside it). Inside it, there is something, but it can be different based on
different factors (Like the user's OS or the time) In simple words, it can
_vary_, hence why we call it a _variable_

In Rust, Variables can either be mutable or immutable.

This means that some variables are allowed to change while others are not.

Mutable means it can change, while immutable cannot be changed. Continuing our
analogy from before, Immutable variables are the glass boxes and are sealed, so
we can only look at what it is. Whereas a mutable variable is not sealed,
allowing you to open it, change whats inside it, and put it back inside

Here is how to define variables, and make them mutable.

```rust
let mut mutable_variable = 0;

let immutable_variable = 0;
```

> Declaring a variable is telling rust that when we use the letter `i` we mean
> the value stored inside `i`

Rust variables are made with the `let` keyword followed by their name By
default, variables are immutable. Making them mutable requires the `mut` keyword

The following code will not throw any errors if you try to run it.

```rust
let mut i = 0;
i = 2;
```

Try removing the `mut` from the code, and then run the code with `cargo run`
