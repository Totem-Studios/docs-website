# Data Types

#### _The Lotus Programming Language_

### Lotus has <u>5</u> primitive data type groups for storing and manipulating data. These groups all have different sizes in memory and everyone except the 'bool' and 'char\*' data types have a size or encoding attached to them.

## Integers

Lets take closer look at the different data types for integer numbers.

```rust
i32
```

The modest `i32` clearly conveys a data type which stores integer values and has a size of 32 bits, or 4 bytes. In languages like C and C++ the size of an `int` may vary depending on the system implementation. In Lotus an `i32` has the same memory footprint independent of the platform.

The rest of the integer data types are:

```rust
i16
```

```rust
i64
```

```rust
i128
```

These data types act similiar to the `short`, `long` and `long long` found in C and C++ however are, just like `i32`, independent of the platform. `i16`, `i64` and `i128` have the sizes of 2 bytes, 8 bytes and 16 bytes respectively.

## Floats

Lets take closer look at the different data types for floating point numbers (decimal numbers).

```rust
f32
```

Just like `i32`, `f32` has a size of 4 bytes but stores floating point numbers, meaning decimal numbers. And just like the `i16`, `i64` and `i128` data types,there is a `f16`, `f64` and `f128` with the same respective sizes.

```
f16
```

```rust
f64
```

```
f128
```

## Characters

Characters in Lotus do not have sizes as in a range, rather there are different encodings such as UTF-8, Unicode.

For regular characters that have a place in the ASCII charset, Lotus uses `char` or `char:ascii`.

```
char:ascii
```

Through this naming it is clear to both the programmer and the compiler what character encoding is meant to take place. A standalone `char` will be interpreted as `char:ascii`.

You specify the encoding accordingly:

```
char:<encoding type>
```

Read more about all the available character encodings [here](../standards/character-encodings.md).
