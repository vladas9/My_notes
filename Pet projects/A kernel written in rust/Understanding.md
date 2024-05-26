---
Date: 2024-05-26
tags:
  - project
  - programming
---
# The main idea 
The main idea of the project is to build a [[Kernel]] in rust programming language.

# Understanding the concept of the project
## Introduction
To write an operating system kernel, I need code that does not depend on any operating system features. This means that I can’t use threads, files, heap memory, the network, random numbers, standard output, or any other features requiring OS abstractions or specific hardware. Which makes sense, since I am trying to write my own OS and our own drivers.
## I can't use rust std
This all mean I can't use rust standard library, but I still can use a lot of features of rust like  iterators, closures, pattern matching, option and result, string formatting, and of course the ownership system. These features make it possible to write a kernel in a very expressive, high level way without worrying about undefined behavior or memory safety.





## References 
1. https://os.phil-opp.com/freestanding-rust-binary/