# ceil-division-in-wild
Example of ceil divisions.

I have collected code that do ceil division (round up after division) from popular open source project using `grep/git grep`.
For example, you can find `(x + y - 1) / y` expression in C (and C like) programming language using following command:
```
git grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+ - 1\) / [[:alnum:]_.]+"
```

In case magic number is used like `(x + 31) / 32`
```
git grep -E "\([[:alnum:]_.]+ \+ [[:digit:]]+\) / [[:digit:]]+"
```

## Implementations of ceil division
x is dividend and y is divisor.
- (x + y - 1) / y
  - Doesn't work with negative numbers
  - Doesn't work if `x + y - 1` overflowed

- x / y + 1
  - results in one higher value in following case
    - x mod y == 0
    - x / y is negative value and integer division is always rounds towards to zero

- (x >> n) + ((x & (2^n - 1)) ? 1 : 0)
  - Assume divisor is a power of 2 number y = 2^n and n >= 0
  - works with any dividend even if it is negative

## Why this repo exists
https://github.com/nim-lang/Nim/pull/18596
