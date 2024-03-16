# Lotus syntax (in the works)

## Loops

### For loops

```
for i32 i = 0; i < 10; i++ {
    print("Number: {i}");
}

for i in 0..10 {
    print("Number: {i}");
}
for e in list {
    print("Element: {e}");
}
```

### While loops

```
while condition {
    print("Still running...");
}
```

## Conditional statements

### If statements

```
if !condition {
    print("It is false");
}

if condition && another_condition {
    print("Both are true");
}

if condition || another_condition {
    print("One is true");
}
```

One line if statements (force the use of parentheses on if statements without braces)

```
if (x == 2 && y < 3) print("x is 2 and y is less then 3");
```

### Else statements

```
if condition {
    // code here
} else {
    // more code here
}
```

### Else-if statements

```
if condition {
    // code here
} else if another_condition {
    // more code here
} else {
    // even more code here
}
```

## Variables

Variables are immutable by default

```
i32 x = 2;
bool y = true;
str z = "hello, world";
```

Use the mut keyword to make them mutable

```
mut i32 x = 2;
mut bool y = true;
mut str z = "hello, world";
x = 3;
y = false;
z = "new str";
```

Using auto to detect the type

```
mut auto x = 23;
```

`Or alternatively using a colon with the type after the variable name`

```
x: i32 = 2;
y: bool = true;
y: str = "hello, world";
```

Use the mut keyword to make them mutable

```
mut x: i32 = 2;
mut y: bool = true;
mut z: str = "hello, world";
x = 3;
y = false;
z = "new str";
```

Using auto to detect the type

```
mut x: auto = 23;
```

## Functions

Function without return type

```
fn printInLoop(str text, i32 n) {
    for i in 0..n {
        print(text);
    }
}
```

Function with return type

```
fn factorial(i32 n) -> i32 {
    if n == 1 {
        ret n;
    }
    ret factorial(n - 1);
}
```

`Or alternatively using a colon with the type after the paramater name`

Function without return type

```
fn printInLoop(text: str, n: i32) {
    for i in 0..n {
        print(text);
    }
}
```

Function with return type

```
fn factorial(n: i32) -> i32 {
    if n == 1 {
        ret n;
    }
    ret factorial(n - 1);
}
```