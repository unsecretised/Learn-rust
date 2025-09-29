# Chapter 1 - Hello, World!

## Notes regarding the book

In many portions of the book, you may see statements like:

```rust
let ignore = 0;
```

It usually implies that the statment is inside a function (like `fn main()`) and
you can simply click the unhide button that appears when you hover over the code
snippet

> Hello world is the first program that most programming languages teach
> beginners. Many tutorials will teach you how to "print" Hello, World! to the
> terminal / console as the first project

---
In rust, everything starts with a main function (annotated with `fn`).
> Ignore what a function is for now. Just imagine a function as a container with things inside it.
  We will cover functions more in Chapter 4

This main function is the entry point of the program.

If you run the program, the main function will be executed.

You can use cargo to create a new project (`cargo new project_name`) and the below code will be preset in src/main.rs.
```rust
fn main() {
    println!("Hello, world!");
}
```
Rust also has it's unique `macros` which are somewhat similar to functions, so you can ignore them for now.

> As of now, I do not plan on covering macros in this book so you might want to check out the official book after this book
to find out more about macros.
---

## Comments

Comments are used to explain the code. The compiler does not care about
comments.

`//` means the rest of the line from this point on is a comment

`/*` and `*/` means everything between is to be ignored / is a comment

You can see how comments are written inside code in this example:

```rust
// This is a single line comment
/* This is a multi-line comment
   It can span multiple lines */
fn main() {
    println!(/*This comment gets ignored by the compiler*/"Hello, World");
    // The above line is equivalent to the below line to the compiler
    println!("Hello, World");
}
```

> The rust community rarely uses multiline comments and usually resorts to
> single line comments more. This is because they are an idiomatic comment
> style.

---
