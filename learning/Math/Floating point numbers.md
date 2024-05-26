---
Date: 2024-05-06
tags:
  - Math
---
# Floating point notation
## Decimal 
Floating point notation is similar to what is called **scientific notation**
A nonzero number x, can be written in the form
$$\LARGE x = \sigma \cdot \bar{x} \cdot 10^e$$
were $\large \sigma = \pm 1$, e is an integer, and $\large 1_{10} \leq \bar x \leq 10_{10}$
Number $\large \sigma$ is called **sign**, e is **exponent**, and $\large  \bar x$ is called **mantissa**.
## Binary
For binary floating point number we have the notation
$$\LARGE x = \sigma \cdot\bar x\cdot 2^e$$
# IEEE
**IEEE** (Institution of Electronics Engineers)
## Single precision standard (32 bits)
Single precision has in mantissa 24 binary digits, exponent e has values between -126 and 127, or in binary $\large -(1111110)_2 \leq e \leq (1111111)_2$
- Basically, $\large\sigma$ is stored as a single bit, the mantissa  $\large\bar x$ as 24 bits (only 23 need to be stored, because first one is always 1)
In order to avoid the sign for exponent, denote
$$\Large E = e + 127, \quad 1 \leq E\leq 254$$
## Double precision standard (64 bits)
Double precision has in mantissa 52 binary digits, exponent e has value between -1022 and 1023 or 11 bits, and the remaining one for $\large \sigma$



## References 
1. [[NA_Lecture1 Part 2.pdf]] 