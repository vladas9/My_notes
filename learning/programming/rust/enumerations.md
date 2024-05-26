---
Date: 2024-04-17
tags:
  - programming
  - rust
---
# Defining an Enum
Where structs give you a way of grouping together related fields and data enums give you a way of saying a value is one of a possible set of values.
- Enums can be declared 
```rust
enum enum_name{
	variant1_name,
	variant2_name,
	...,
}
```
- We can create a instance of a variant like this: `let name = enum_name::variant_name`
	- [i] Also enums type can be used in functions as taken or return value
- Also enums can be defined with specific type, like this:
```rust
 enum IpAddr {
        V4(String),
        V6(String),
}

// or with different types
  enum IpAddr {
        V4(u8, u8, u8, u8),
        V6(String),
}

// Also as a type can be a structure
struct Ipv4Addr {
    // --snip--
}

struct Ipv6Addr {
    // --snip--
}

enum IpAddr {
    V4(Ipv4Addr),
    V6(Ipv6Addr),
}
```

# The Option Enum

Option is another enum defined by the standard library. The Option type encodes the very common scenario in which a value could be <mark style="background: #FFF3A3A6;">something</mark> or it could be <mark style="background: #FFF3A3A6;">nothing</mark>.

Rust does not have nulls, but it does have an enum that can encode the concept of a value being present or absent. This enum is `Option<T>`, and it is defined by the standard library as follows:
```rust
enum Option<T> {
    None,
    Some(T),
}
```
> [!note]
> `<T>` means that the `Some` variant of the `Option` enum can hold one piece of data of any type, and that each concrete type that gets used in place of `T` makes the overall `Option<T>` type a different type.
## References 
1. https://doc.rust-lang.org/book/ch06-00-enums.html