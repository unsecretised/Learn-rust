# Chapter 2 - Variables

Try to understand the below statement. It's ok if you don't get it, it's
explained afterwards

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

```rust
let i = 0;
i = 2;
```

What error does it give?

It should be similar to:

```
Compiling playground v0.0.1 (/playground)
error[E0384]: cannot assign twice to immutable variable `i`
 --> src/main.rs:4:1
  |
3 | let i = 0;
  |     - first assignment to `i`
4 | i = 2;
  | ^^^^^ cannot assign twice to immutable variable
  |
help: consider making this binding mutable
  |
3 | let mut i = 0;
  |     +++

For more information about this error, try `rustc --explain E0384`.
error: could not compile `playground` (bin "playground") due to 1 previous error
```

The error message: `cannot assign twice to immutable variable i` means that we
cannot give i a value twice (or in other words, cannot change its value)
Therefore, `i` is an immutable variable. Notice how we didn't have to specify
that `i` is an immutable variable. That's because by default, all variables are
considered immutable. This is a feature exclusive to rust.

> If you have experience with other coding languages, you may wonder why Rust
> has this feature and the reason is simple. Some variables are meant to be the
> same throughout the program. And Rust is the teacher holding a stick waiting
> to make sure you don't change something you aren't meant to change in the
> future. There are some more advanced reasons that you can have a look at once
> you're more experienced with Rust.

## Type definitons

A variable in rust can only be of a certin type, or in other words, the glass
box's size is fixed, and cannot be changed.

Some types in rust are:

- `String` & `&str` (These are different types but both are String types, which
  are used for storing text)
- `Vec<T>` (Ignore the `<T>` for now, just imagine it as saying that its a Vec
  of a type with `T` as a placholder) We will discuss this more later in this
  chapter.
- `i8`, `i16`, `i32`, `i64`, and `i128`. In simple terms, each of these types
  store a negative / postitive number with a limit of `2^32` as the max value if
  its `i32`
- `u8`, `u16`, `u32`, `u64` and `i128`. This is the same as the `i` series, but
  it can only store positive numbers.
- The `f` series, which stores decimal numbers, like `22.1`, etc.

You specify a Variables type in the following manner:

```rs
let string: Type = SomeValueHere;
```

Let's go through all the above mentioned types and their definitions.

```rs
let string_1: &str = "Something"; // &str
let string_2 = "This is also an &str"; // &str

let string_3: String = String::from("a String type is used to store text"); // String
let string_4 = "Another way to define a String".to_string();
```

Let's unpack each line one by one.

1. After telling rust that we are making a variable with `let`, we go into
   saying that `string_1` should have a type of `&str` ("the shape of the box")
   with `: &str` and then we "put something inside the box" with
   `= "Something"`.
1. In the second line, we talk don't tell Rust that we want a `&str`. This is
   Rust automatically selecting the box shape, hence why these type's aren't
   needed most of the time.
1. In the third line, we see a new type called `String`. This is slightly
   different from `&str` but for now we will treat it as the same wherever
   possible. Defining a `String` requires us to either use `String::from()` or
   do: `"&str here".to_string()` which tells rust to convert a `&str` to a
   `String`

## Using Variables

Variables can be used by their names. For example, when we are creating a
`String` we can make an `&str` into a string with `.to_string()`. Here's an
example:

```rs
let example = "Rust is so Fun!!";
let example_as_a_string = example.to_string();
```

You can also do:

```rs
let another_example = String::from(example);
```

and it will work the exact same way.

## Other variable types:

### The `i` Series

```rs
let i_8: i8 = 1;
let i_16: i16 = -14;
let i_32 = 45; // Notice how we don't specify i32 here? i32 is the default for numbers in rust.
let i_64: i64 = -6493;
let i_128: i128 = -128231;
```

### The `u` Serise:

```rs
let u_8: u8 = 1;
let u_16: u16 = 14;
let u_32: u32 = 45; 
let u_64: u64 = 6493;
let u_128: u128 = 128231;
```

### The `f` Series:

```rs
let f_8: f8 = 0.1;
let f_16: f16 = 0.1;
let f_32: f32 = 0.1;
let f_64 = 0.1; // Floating point types are automatically inferred as f64's, but you can also explicitly define them.
let f_128: f128 = 0.1;
```

> Despite humanity having achieved amazing feats, accurate floating point
> mathematical operations are not one of them. The reason is kind of blurry to
> me as well, so here's a
> [YouTube Video](https://youtu.be/2gIxbTn7GSc?si=w5pT5SaGf19AxXuz) you can use
> to understand why if you are interested. While the reason is not neccessary to
> know for now, I recommend knowing that floating point arithmetic is one the
> biggest weak points in computers.

## `Vec` Data Type

Earlier in this chapter, I mentioned a `Vec<T>` where `T` is a placeholder for a
type. This is called a Vector or in other languages, called Array. In real life
`Array` and `Vector` do have a few differences, however for simplicity reasons,
you can consider them the same.

A Vector can be thought of as a "List" of items (You may also here people use
the word `list` as an alternative to arrays) It stores an unknown amount of
data. (The limit is how much your hardware supports)

In rust, there are a many ways to make a Vector, but I will show you only one.
The other ways are more complex, and you would probably want to take a look at
[the book](https://doc.rust-lang.org/book) for that.

The most simple way to make a Vector is with `vec![]`
```rs
let odd_numbers = Vec![1,3,5,7,9];
```

> Remember the `<T>`? What if we were to specify a type for a vector?

```rs
let str_excl: Vec<&str> = vec!["", "Another element", "Another"];
```

This tells rust that we want a Vector that stores `&str`'s inside it.
