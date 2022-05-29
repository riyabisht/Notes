---
layout: default
title: Bit Manipulation
parent: Competitive Programming
---

# Bit manipulation

1. TOC
{:toc}

Bit manipulation refers to changing the bit of the binary number.

Some common bitwise operators provided by many programming languages are:

- and `&`
- or `|`
- xor `^`
- not `~`
- right shift `<<`
- left shift `>>`

Don't confuse bitwise operator with logical operators.
Logical operators are:

- ans `&&`
- or `||`
- not `!`

Let's start by a simple task, printing binary of a number:

```cpp
void print(int n) {
    for(int i=10;i>=10;--i){
        cout << ((n>>i)&i);
    }
}
```

## Check if a number is even or odd

```cpp
if(n&1)
    cout << "No is odd";
else
    cout << "No is even";
```

## Multiply and divide a number by 2

```cpp
// multiply by 2
n = n<<1;

// divide by 2
n = n >> 1;
```

## Convert a character for lower to upper case and vice versa

```cpp
c = 'a';
upper = c^32;
```