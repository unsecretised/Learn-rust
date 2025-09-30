# Welcome to Rust!

## About this book:

### Important notice #0:

This book is meant to be for people new to programming and want to learn rust.
Despite being an avid rust lover, I will advise you to not learn rust. In fact,
Rust has so many complex concepts that take even the most advanced developers
time to truly understand. My advice would be to learn the basics of python and /
or JavaScript, and then come back to rust. However, if you are stubborn like
many developers (and me), then you are welcome to use this book and try to learn
rust.

### Important notice #1:

This book has been simplified and some deeper explanations has been skipped. My
advice would be to use this book, but then once you have the basics down, take
on the challenge of using [the official book](https://doc.rust-lang.org/book)
which should be significantly easier to understand as they use more
technological terms in comparison to this book.

### Just some boring stuff about me:

This book, is not affiliated with any company / foundation / organisation. It is
currently a solo project by a 17-year-old rust developer, who had trouble
learning rust from the book due to its extreme amounts of terminology used, and
wants to help others learn rust as well. If you are a person from the rust
foundation, then I would really appreciate it if you could try and voice this
project out for me.

# Installation / Alternatives

I would recommend [installing Rust](https://rust-lang.org/tools/install) which
will also install cargo. However, you can also use the
[rust playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2024)
for the first few chapters. However, after a certain point of time (chapter 4's
modules section) It would be required to install Rust to make your life easier.

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

## Recommended Additional Resources:

- [Discord](https://discord.gg/rust-lang-community) - This discord is filled
  with a bunch of smart hackers, (and me) and you will be able to ask any of
  your questions and get help with understanding various concepts with the help
  from others. However, they will only help you, if you are willing to help
  yourself, by using google if you can.
- [Official Book](https://doc.rust-lang.org/book/) - This is the official rust
  book. This current book, is a dumbed down version, with some of the advanced
  chapters skipped.
