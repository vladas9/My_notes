---
Date: 2024-04-08
tags:
  - rust
  - programming
links: https://doc.rust-lang.org/book/ch05-03-method-syntax.html
---
_Methods_ are similar to functions: we declare them with the `fn` keyword and a name, they can have parameters and a return value, and they contain some code that’s run when the method is called from somewhere else. Unlike functions, methods are defined within the context of a struct, and their first parameter is always `self`, which represents the instance of the struct the method is being called on.

## Defining methods
```rust
impl struct_name{
	fn method_name(){
	}
}
```
## Calling method
Rust uses a period(.) to access a method and doesn't have a -> for pointers   
Here’s how it works: when you call a method with `object.something()`, Rust automatically adds in `&`, `&mut`, or `*` so `object` matches the signature of the method. In other words, the following are the same:

```rust
p1.distance(&p2);
(&p1).distance(&p2);
```