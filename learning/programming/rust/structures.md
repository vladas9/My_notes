---
Date: 2024-04-08
tags:
  - rust
  - programming
links: https://doc.rust-lang.org/book/ch05-01-defining-structs.html
---

A _struct_, or _structure_, is a custom data type that lets you package together and name multiple related values that make up a meaningful group.

Structs are similar to [tuples](data-types(rust).md#Tuples), in that both hold multiple related values. Like tuples, the pieces of a struct can be different types. Unlike with tuples, in a struct you’ll name each piece of data so it’s clear what the values mean.

Structure definition:
```rust
struct Name {
    var_name: type,
    ...
}
```
Example:
```rust
struct User {
    active: bool,
    username: String,
    email: String,
    sign_in_count: u64,
}
```
To use a struct after we’ve defined it, we create an _instance_ of that struct by specifying concrete values for each of the fields. We create an instance by stating the name of the struct and then add curly brackets containing _key: value_ pairs, where the keys are the names of the fields and the values are the data we want to store in those fields.
- [i] We don’t have to specify the fields in the same order in which we declared them in the struct.

Example:
```rust
let user1 = User {
        active: true,
        username: String::from("someusername123"),
        email: String::from("someone@example.com"),
        sign_in_count: 1,
    };
```

To access the data from struct should be used a period(.)
```rust
 user1.email
 user1.active
```

#### Using the Field Init Shorthand

If the parameter names and the struct field names are exactly the same we can use the _field init shorthand_ syntax
```rust
fn build_user(email: String, username: String) -> User {
    User {
        active: true,
        username,
        email,
        sign_in_count: 1,
    }
}
```

### Creating Instances from Other Instances with Struct Update Syntax

It’s often useful to create a new instance of a struct that includes most of the values from another instance, but changes some. You can do this using _struct update syntax_.
```rust
let user2 = User {
        email: String::from("another@example.com"),
        ..user1
    };
```
In this example only the email parameter is unique and other ones are the same as in user1

### Using Tuple Structs Without Named Fields to Create Different Types
Rust also supports structs that look similar to tuples, called _tuple structs_. Tuple structs have the added meaning the struct name provides but don’t have names associated with their fields; rather, they just have the types of the fields.
```rust
struct Color(i32, i32, i32);
struct Point(i32, i32, i32);
```
### Unit-Like Structs Without Any Fields
You can also define structs that don’t have any fields! These are called _unit-like structs_ because they behave similarly to `()`
```rust
struct AlwaysEqual;
```

Also for structures can be defined [[methods]]