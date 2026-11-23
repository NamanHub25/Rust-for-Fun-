# What exaclty is Rust ?
- Rust is a statically typed, compiled systems programming language

**A. Statically typed**
- Every value has a type, and Rust checks types during compilation.

For example:

```rust
let age: i32 = 21;
```
Here, **i32** represents a signed 32-bit integer.

**B. Compiled Language**
- Rust code isn't directly executed as a source code, the compiler translates our source code into the machine-executable instructions

**C. Systems Programming Language**
Rust provides control over memory, resource management and low-level operations.

This makes it suitable for:
- Operating systems.
- Command-line utilities.
- Databases.
- Networking infrastructure.
- Web servers.
- Embedded systems.

# Understanding the Rust toolchain
- There are three important tool we must distinguish


| Tool | Responsibility |
| :--- | :--- |
| `rustup` | Installs and manages Rust toolchains |
| `rustc` | Compiles Rust source code |
| `cargo` | Manages projects, dependencies and builds |

Think of cargo as your project manager, rustc as your rust compiler and rustup as your toolchains manager 

# First Rust program 

```rust
fn main() {
    println! ("Hello, its getting Rusty here...");
}
```

`fn main()`
- fn is the keyword used to define a function.
- main is the special name of the function where a Rust executable program begins running.
- The curly braces {} contain the function's body.

`println!("Hello, world!");`
- println! prints text to the terminal.
- The ! is important: println! is a Rust macro, not an ordinary function.
- The text inside the quotation marks is what we want to display.
- The semicolon ; marks the end of this statement.