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

---

## Installation / Alternatives

I would recommend installing [Rust](https://rust-lang.org/tools/install) which
will also install cargo.

Use this with VSCode or any IDE / Code editor of your choice. I recommend
[VSCode](https://code.visualstudio.com) or [Zed](https://zed.dev)

## Setup

Creating a new project happens via the command line.

I've made a step by step guide on how I recommend you to create a new project.

1. Create a folder to store your projects with your file explorer / finder
1. Launch VSCode (or Zed), then click on File > Open Folder > Select the folder
   you just created
1. Then open the terminal with CMD + \` (MacOS) or CTRL + \` (Windows / Linux)
1. Here, run `cargo --version` to ensure that you have cargo installed.
1. If you do not have rust installed, you can install it from
   [here](https://rust-lang.org/tools/install)
1. Then run `cargo new hello_world` to create a new rust project called
   hello_world (You can change the name in the future according to what you want
   to call your project)
1. Then open the project in VSCode the same way you opened the projects folder
   (Step 2)
1. Then run `cargo run` to run your project
