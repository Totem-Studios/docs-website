# Data Types

#### _The Lotus Programming Language_

### Lotus has <u>5</u> primitive data type groups for storing and manipulating data. These groups include:

# i

- Integer numbers

# f

- Floating point numbers

# char

- Characters

# c\*

- Character strings

# bool

- Booleans

### These groups all have different sizes in memory and everyone except the 'bool' and 'c\*' data types have a size attached to them.

## integers

Lets take closer look at the different sizes for 'i', integer numbers.

```rust
i32
```

The modest `i32` clearly conveys a data type which stores integer values and has a size of 32 bits, or 4 bytes. In languages like C and C++ the size of an 'int may vary depending on the system implementation. In Lotus an `i32` has the same memory footprint independent of the platform.

The next two sizes are the `i64` and `i128`.

```rust
i64
```

```rust
i128
```

These data types act similiar to the `long` and `long long` found in C and C++ however are, just like `i32`, independent of the platform. `i64` and `i128` have the sizes of 8 bytes and 16 bytes respectively.

## floats

Lets take closer look at the different sizes for 'f', floating point numbers.

```rust
f32
```

Just like `i32`, `f32` has a size of 4 bytes but stores floating point numbers, meaning decimal numbers. And just like `i64` and `i128` there is a `f64` and a `f128` with the same respective sizes. Floating point numbers in Lotus have, just like any other programming language, a trade-off when it comes to accurracy and range.

```rust
f64
```

```
f128
```

## characters

Characters in Lotus do not have sizes as in a range, rather there different encodings like UTF-8, Unicode etc.

For regular characters that have a place in the ASCII charset, Lotus uses `c_ascii`.

```
char::ascii
```

Through this naming it is clear to both the programmer and the compiler what character encodui

```
char::utf8
```

```
char::unicode
```
