# Roman to Integer

A simple Java program that converts Roman numerals to integers.

## Description

The `romanToInt(String s)` function takes a string of Roman numerals and returns its value as an `int`.

The algorithm scans the string from left to right:

- if the value of the current symbol is **less than** the value of the next one (e.g. `I` before `V`), it is **subtracted** from the result,
- otherwise it is **added**,
- finally, the value of the last symbol is added.

Symbol values are stored in a `HashMap<Character, Integer>`.

## Symbol Values

| Symbol | Value |
|--------|-------|
| I      | 1     |
| V      | 5     |
| X      | 10    |
| L      | 50    |
| C      | 100   |
| D      | 500   |
| M      | 1000  |

## Requirements

- Java 25 or newer (the program uses unnamed classes, instance main methods, and `IO.println`)

## Usage

```bash
java Main.java
```

## Example

```java
IO.println(romanToInt("MCMXCIV"));
```

Output:

```
1994
```

Breakdown: `M` (1000) + `CM` (900) + `XC` (90) + `IV` (4) = **1994**.

## Complexity

- Time: **O(n)**, where *n* is the length of the string
- Space: **O(1)** (a fixed map of 7 entries)

## Limitations

- The program assumes valid Roman numeral input (no input validation).
- An empty string or characters outside `I V X L C D M` will cause an exception.

## License

This project is provided for educational purposes.
