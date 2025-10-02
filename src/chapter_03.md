# Chapter 3 - Control Flow

In programming, control flow usually means one of the following:

- `if` a condition is met, then we do something.
- `else if` - If the previous condition are not
- `else` do something else

- `while` a certain condition is met, keep executing the code.
- `for` every item inside a Vector, do something with the item. (For loops are
  not restricted to Vector's as we will see later)

Let's start with the `if`, `else if` and `else` statements.

Let's quickly cover another data type called `bool`, or Boolean. A Boolean
stores just 2 possible values, `true` or `false`.

```rust
let yes = true;
let no: bool = false;
```

An `if` statement checks if something evaluates to `true` (a condition is met)
or `false` (a condition is not met)

An `else if` statement is a continuation to an if statement, which is like, `if`
the previous conditions are **NOT** met, but the condition in the `else if` is
met, then the code gets executed.

An `else` statement is for, when none of the conditions get met, then this code
gets reached, and executed.

Try playing around with the code below, and try to get all the conditions met.

```rust
let condition = true;

if condition {
    println!("This condition is true.");
} else if !condition { // ! reverses the condition, AKA true becomes false and false becomes true
    println!("The condition is not true");
} else {
    println!("Can this statement be reached?");
}
```

> Could you reach all the conditions? If you managed to reach the last
> condition... please be careful. You have probably been put under a watchlist.
> The last else statement was

If you notice, the last condition is impossible to reach. This is because we are
using a boolean for comparison directly, hence one of the first 2 conditions
will be met. So what's the use of `else if` and `else`?

Let's see another example, where we use strings instead of booleans. But how do
we use strings here? We use comparison operators. We will start with the basic
ones, `==` and `!=`.

```rust
let string_comparison = "input_2";

if string_comparison == "input_1" {
    println!("Input");
} else if string_comparison != "input_2" {
    println!("Neither input 1 or 2");
} else {
    println!("It's Input 2");
}
```

In Rust, we have a better way for doing such comparisons. It's called a `match`
statement.

Let's try doing the same string comparison but with this `match` statement:

```rust
let string_comparison = "input_2";

match string_comparison {
    "input_1" => println!("String comparison is input_1"),
    "input_2" => println!("String comparison is input_2"),
    _ => println!("String comparison is Neither input 1 or 2"),
}
```

In match statements, each comparison is done via the concept of `arms`. Each
"arm" is a case that rust will check for the correct value. However, covering
all cases is required, and if you want to do `else` case arm, then you use
either `_` or you can do:

```rust
match "abc" {
    a => println!("{}", a),
}
```

Now let's move onto the next statement, `while` loops. `while` loops allow for a
specific funtion to get repeated until that condition is no longer true.

```rust
let mut count = 0;

while count < 10 {
    println!("The count is at: {}", count);
    count += 1; // this statement is equivalent to count =  count + 1
}
```

> In the above code, we use a `count += 1` which basically evaluates to set
> `count` to the current value of `count + 1`. You can replace the `+` operator
> with `-` for minus, `*` for multiplication, or `/` for division.


