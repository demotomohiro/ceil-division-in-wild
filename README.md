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

Some code use `x / y + 1` for ceil division but that results in one higher value when x is divisible by y or x is 0.

## Why this repo exists
https://github.com/nim-lang/Nim/pull/18596
