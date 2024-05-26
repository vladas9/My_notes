---
tags:
  - rust
  - programming
---
## Variables
In rust all variable can be reused by re declaring them, also using it the [data type](data-types(rust).md) of the variable can be changed and  also the variable can become mutable from immutable
```rust
let spaces = "  "; //string literal
let spaces = spaces.len();  //i32
let mut spaces = 5; // mutable variable
```
## Functions
Rust function are created using **fn** key word, the function syntax looks like this
```rust
fn <function name>(<variable name>: <data type> ...) -> <return data type>{
function body
}
```
## Control flow
### If/else
Syntax
```rust
if <condition>{
//if contiton is true
}else{
//if condition is false
}
```
Also if statement can be used in let
Example:
```rust
let number = if condition { 5 } else { 6 };
```
NOTE: the type in if and else block should be the same

### Loop
The `loop` keyword tells Rust to execute a block of code over and over again forever or until you explicitly tell it to stop([break](Key-words(rust).md)).
Syntax 
```rust
loop{
// Body
}
```
The [break](Key-words(rust).md) and [continue](Key-words(rust).md) key word will be applied to the innermost loop at that point, so there are several nested loops the loop can be labeled for a better specification
Label syntax: '/label name/: loop, example:
```rust
'counting_up: loop { 
	println!("count = {count}"); 
	let mut remaining = 10; 
	loop { println!("remaining = {remaining}"); 
		if remaining == 9 { break; } 
		if count == 2 { break 'counting_up; } 
		remaining -= 1; 
		} 
	count += 1; 
}
```
### While
A conditioned loop
Syntax
```rust
while <cindition>{
	//loop body
}
```
### For
For loop is used to iterate over collections 
Syntax
```rust
for item in collection {     
// body of the loop 
}
```