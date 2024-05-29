---
Date: 2024-05-26
tags:
  - project
  - programming
  - rust
  - low_level
---
# Rust   implementation
## The no_std Attribute
As I said in [[Understanding]] I can use rust standard library. The reasons are, when building a kernel in Rust, cannot be used the standard library (`std`) because it depends on OS-provided services for functionality, which are not available at the kernel level, requiring  to manage memory, threading, and hardware access directly.
- So to remove the std from my rust program i can use `#![no_std]` attribute. 
## Panic Implementation
The panic_handler attribute defines the function that the compiler should invoke when a panic occurs. The standard library provides its own panic handler function, but in a no_std environment we need to define it ourselves:
```rust
use core::panic::PanicInfo;

/// This function is called on panic.
#[panic_handler]
fn panic(_info: &PanicInfo) -> ! {
    loop {}
}
```
The PanicInfo parameter contains the file and line where the panic happened and the optional panic message. The function should never return, so it is marked as a diverging function by returning the “never” type !. There is not much we can do in this function for now, so we just loop indefinitely.





## References 
1. https://os.phil-opp.com/freestanding-rust-binary/