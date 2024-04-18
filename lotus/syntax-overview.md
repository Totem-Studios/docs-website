# Lotus syntax (in the works)

## Variables

Variables are immutable by default

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

Use auto or the walrus operator to detect the type

```
x: auto = 23;
x := 23;
```

`Or alternatively using the type before the name`

```
i32 x = 2;
bool y = true;
str z = "hello, world";
```

```
mut i32 x = 2;
mut bool y = true;
mut str z = "hello, world";
x = 3;
y = false;
z = "new str";
```

```
auto x = 23;
x := 23;
```

## Loops

### For loops

```
for i: i32 = 0; i < 10; i++ {
    print(f"Number: {i}");
}

for i in 0..10 {
    print(f"Number: {i}");
}
for e in list {
    print(f"Element: {e}");
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

`Or alternatively using "and", "or" and "not"`

```
if not condition and (another_condition or a_third_condition) {
    print("Result is true!");
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

## Functions


Function without return type

```
fn print_in_loop(text: str, n: i32) {
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

`Or alternatively using the type before parameter name`

```
fn print_in_loop(str text, i32 n) {
    for i in 0..n {
        print(text);
    }
}
```

```
fn factorial(i32 n) -> i32 {
    if n == 1 {
        ret n;
    }
    ret factorial(n - 1);
}
```

## Type casting

Cast a variable with: \<variable\> ~ \<type\>

```
x: f64 = 3.4;
y: i32 = x ~ i32;
```

## F-strings

Use an f-string to insert variables inside of a string (useful when printing)

```
age: i32 = 10;
print(f"Your age is: {age}");
```
