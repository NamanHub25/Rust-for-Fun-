# Cargo
- So far, we have used rustc directly to compile a single Rust file. That works perfectly for small programs. But imagine building a backend application with 30 source files and 10 external libraries. Managing compilation and dependencies manually would quickly become inconvenient. That's where Cargo comes in.

## What exactly is Cargo ?
Your book describes Cargo as Rust's build system and package manager.

Let's understand both responsibilities.
- **Build system:** Cargo helps compile your source code and produce executable programs.
- **Package manager:** Cargo manages the libraries your project depends on, including downloading and building them.
In Rust, packages of code are referred to as `crates.` When your application needs an external library, that library becomes a dependency of your project.

For example, our upcoming `Guessing Game` will use an external crate to generate random numbers.

The command:
```rust
cargo new hello_cargo
```
enables cargo to create a project for us with the name hello_cargo, let's understand the project structure

**Cargo.toml** — Project configuration
This is one of the most important files in a Rust project.

The book shows a generated configuration similar to this:
```rust
[package]
name = "hello_cargo"
version = "0.1.0"
edition = "2021"

[dependencies]
```
Let's break this down

| Element | Purpose |
| :--- | :--- |
| `[package]` | Starts the package configuration section |
| `name` | Name of your package |
| `version` | Current package version |
| `edition` | Rust edition used by the package |
| `[dependencies]` | Where you declare external crates your project needs |

**What is TOML?**

`TOML` stands for *Tom's Obvious, Minimal Language.* It's a configuration-file format used by Cargo.

For now, remember this:

Cargo.toml tells Cargo about your project and its dependencies.
src/ — Where your source code lives
The book explains that Cargo expects your source files to live inside the src directory.
