---
tags:
  - rust
  - programming
---
Rust has two data type subsets: scalar and compound.
## Scalar types
- [[#Integers]]
- [[#Floating-point]]
- [[#Boolean]]
- [[#Character]]
## Compound types
- [[#Tuples]]
- [[#Array]]

### Integers 

| Length  | Signed  | Unsigned |
| ------- | ------- | -------- |
| 8-bit   | `i8`    | `u8`     |
| 16-bit  | `i16`   | `u16`    |
| 32-bit  | `i32`   | `u32`    |
| 64-bit  | `i64`   | `u64`    |
| 128-bit | `i128`  | `u128`   |
| arch    | `isize` | `usize`  |

Each signed variant can store numbers from $-2^{(n - 1)}$ to $2^{(n - 1)} - 1$ inclusive, where $n$ is the number of bits that variant uses. So an `i8` can store numbers from $-128$ to $127$. Unsigned variants can store numbers from $0$ to $2^n - 1$, so a `u8` can store numbers from $0$ to $255$.

##### Integer Overflow
If to an integer will be assigned a value bigger than it's capacity it will overflow and the variable will become the bottom border variable + the value of overflow 

### Floating-point
Exists `f32` and `f64` , singes precision and double

### Boolean
**True** or **False**

### Character
Char literal has single quotes(' ') and can store one Unicode symbol

### Tuples
A _tuple_ is a general way of grouping together a number of values with a variety of types into one compound type. Tuples have a fixed length: once declared, they cannot grow or shrink in size.
**Creating a tuple**
```rust
let tup: (i32, f64, u8) = (500, 6.4, 1);
```
Also the tuple can be discomposed to variables
```rust
let tup = (500, 6.4, 1); // Initial tuple
let (x, y, z) = tup; // x = 500; y = 6.4; z = 1;
```
A element from a tuple can be accessed by using the period (.) flowed by the index of element
```rust
let x: (i32, f64, u8) = (500, 6.4, 1); 
let five_hundred = x.0; 
let six_point_four = x.1; 
let one = x.2;
```

### Array
Unlike a tuple, every element of an array must have the same type. Arrays in Rust have a fixed length.
**Creating an array**
```rust
let a = [1, 2, 3, 4, 5];
```
Also the type and dimension of the array can be specified at creating
```rust
let a: [i32; 5];
```
Were `i32` is the type and `5` is the number of elements.
You can also initialize an array to contain the same value for each element by specifying the initial value, followed by a semicolon, and then the length of the array in square brackets, as shown here:
```rust
let a = [3; 5];
```
**Accessing Array Elements**
The elements of the array can be accessed by using \[index]
```rust
let a = [1, 2, 3, 4, 5]; 
let first = a[0]; 
let second = a[1];
```
