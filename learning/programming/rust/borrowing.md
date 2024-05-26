---
tags:
  - rust
  - programming
---
### Borrowing and References

Borrowing allows you to pass a reference to a value without transferring ownership. There are two types of references in Rust: immutable references (`&T`) and mutable references (`&mut T`).

#### Immutable References

Immutable references allow you to read the value but not modify it. You can have multiple immutable references to the same value, but you cannot have an immutable reference and a mutable reference to the same value at the same time:
```rust
fn main() {
    let s = String::from("hello");
    let r1 = &s;           // immutable reference
    let r2 = &s;           // another immutable reference
    println!("r1: {}, r2: {}", r1, r2);
} // r1 and r2 go out of scope, but since they are just references and do not own the value, nothing happens
```

#### Mutable References

Mutable references allow you to modify the value. However, Rust ensures that you can have either one mutable reference or any number of immutable references, but not both at the same time:
```rust
fn main() {
    let mut s = String::from("hello");
    let r1 = &mut s;       // mutable reference
    // let r2 = &s;         // This would cause a compile-time error
    println!("r1: {}", r1);
} // r1 goes out of scope, allowing s to be used again
```
### Rules of Borrowing

- You can have either one mutable reference or any number of immutable references to a value, but not both at the same time.
- References must always be valid. Rust ensures this at compile time, preventing dangling references.

### Borrowing in Function Parameters

Borrowing is commonly used in function parameters to pass values by reference without taking ownership. For example:
```rust
fn calculate_length(s: &String) -> usize {
    s.len()
}

fn main() {
    let s = String::from("hello");
    let len = calculate_length(&s); // Pass a reference to s
    println!("The length of '{}' is {}.", s, len);
}
```

Borrowing is a key concept in Rust's ownership system, allowing for safe and efficient sharing of data without the need for garbage collection or manual memory management. Understanding borrowing is crucial for writing correct and idiomatic Rust code.