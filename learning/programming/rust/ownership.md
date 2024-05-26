---
tags:
  - rust
  - programming
---
_Ownership_ is a set of rules that govern how a Rust program manages memory.
### Ownership Rules
First, let’s take a look at the ownership rules. Keep these rules in mind as we work through the examples that illustrate them:

- Each value in Rust has an _owner_.
- There can only be one owner at a time.
- When the owner goes out of scope, the value will be dropped.

### Variable scope 
As a first example of ownership, we’ll look at the _scope_ of some variables. A scope is the range within a program for which an item is valid.
```rust
{ // s is not valid here, it’s not yet declared
	let s = "hello";   // s is valid from this point forward
	// do stuff with s
} // this scope is now over, and s is no longer valid
```
In other words, there are two important points in time here:
- When `s` comes _into_ scope, it is valid.
- It remains valid until it goes _out of_ scope.
### Ownership and Move Semantics

In Rust, ownership follows the principle of move semantics. When a variable is assigned to another variable or passed to a function, the ownership of the original variable is moved. This means that the original variable is no longer valid after the move:

```rust
fn main() {     
	let s1 = String::from("hello");
	let s2 = s1;  // s1's ownership is moved to s2     
	// println!("s1: {}", s1); // This would cause a compile-time error     
	println!("s2: {}", s2); // s2 owns the value now 
	}
```
### Returning Ownership

Functions can also transfer ownership back to the calling code using the return value:
```rust
fn give_ownership() -> String {     
	let s = String::from("hello");
	s  // ownership of s is moved to the calling function
}  

fn main() {
	let s1 = give_ownership();
	println!("s1: {}", s1); 
}
```

### Ownership and Copy Types

For types that implement the `Copy` trait, like integers, ownership is not moved but copied. This allows you to continue using the original variable after assigning it to another variable or passing it to a function:
```rust
fn main() { 
	let x = 5;     
	let y = x;  // x is copied, not moved     
	println!("x: {}, y: {}", x, y); // Both x and y can be used 
}
```
Understanding ownership is crucial in Rust to ensure memory safety without the need for a garbage collector. It allows Rust to guarantee at compile time that memory is managed correctly, preventing issues such as dangling pointers and double frees.