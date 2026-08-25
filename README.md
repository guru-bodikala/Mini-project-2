# Implementation of Custom `atoi()` and `atof()` Functions in C

## 📌 Project Overview

This project demonstrates the implementation of custom versions of the standard C library functions **`atoi()`** and **`atof()`** without using any built-in conversion functions.

- **`my_atoi()`** converts a string into an integer.
- **`my_atof()`** converts a string into a floating-point number (`double`).

The program automatically detects whether the input contains a decimal point (`.`):
- If **yes**, it calls `my_atof()`.
- Otherwise, it calls `my_atoi()`.

---

## 🎯 Objective

- Understand how string-to-number conversion works internally.
- Implement custom conversion functions without using library functions like `atoi()` and `atof()`.
- Practice pointer manipulation and command-line arguments in C.

---

## 🛠️ Technologies Used

- Programming Language: **C**
- Compiler: GCC
- Operating System: Linux / Ubuntu

---

## 📂 Project Structure

```
.
├── atoi_atof.c
└── README.md
```

---

## ⚙️ Compilation

Compile the program using GCC:

```bash
gcc atoi_atof.c -o convert
```

---

## ▶️ Execution

### Integer Input

```bash
./convert 12345
```

**Output**

```
12345
```

---

### Negative Integer

```bash
./convert -456
```

**Output**

```
-456
```

---

### Floating Point Input

```bash
./convert 123.456
```

**Output**

```
123.456000
```

---

### Negative Floating Point

```bash
./convert -98.76
```

**Output**

```
-98.760000
```

---

## 💡 Working

### `my_atoi()`

- Checks for negative sign.
- Reads each character until a non-digit is found.
- Converts ASCII digits into integer values.
- Returns the integer result.

### `my_atof()`

- Checks for negative sign.
- Converts the integer part before the decimal point.
- Converts the fractional part after the decimal point.
- Uses a decimal multiplier (`0.1`, `0.01`, `0.001`, ...) to compute the fractional value.
- Returns the floating-point result.

---

## ✨ Features

- Custom implementation of `atoi()`
- Custom implementation of `atof()`
- Supports positive numbers
- Supports negative numbers
- Supports floating-point values
- Uses command-line arguments
- No use of standard conversion library functions

---

## ⚠️ Limitations

- Does not validate invalid input strings.
- Scientific notation (e.g., `1.2e3`) is not supported.
- Leading or trailing spaces are not handled.
- Only one decimal point is supported.

---

## 📚 Concepts Used

- Functions
- Pointers
- Strings
- Command-line arguments (`argc`, `argv`)
- ASCII to numeric conversion
- Loops
- Conditional statements


## 📄 License

This project is created for educational and learning purposes.
