# Primes | A Software Drag Race

From:
https://github.com/PlummersSoftwareLLC/Primes

Ceil division is used in the sieve of eratosthenes to get array length from number of bits needed and bits per int.
Some code uses x div y + 1 for approximated round up.

## Commands to get a list of lines that do ceil division

```
git clone --depth 1 https://github.com/PlummersSoftwareLLC/Primes.git
cd Primes
git grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+ - 1\) / [[:alnum:]_.]+" > x_y-1_div_y
git grep -E "\([[:alnum:]_.]+ / [[:alnum:]_.]+\) \+ 1" > x_div_y_1
git grep -E "\([[:alnum:]_.]+ \+ [[:digit:]]+\) / [[:digit:]]+" > x_n-1_div_n
```
