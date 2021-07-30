# Arraymancer

From:
https://github.com/mratsim/arraymancer
https://mratsim.github.io/Arraymancer

## Commands to get a list of lines that do ceil division

```
git clone --depth 1 https://github.com/mratsim/Arraymancer.git
cd Arraymancer
git grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+ - 1\) div [[:alnum:]_.]+" > x_y-1_div_y
git grep -E " div [[:alnum:]_.]+\)? \+ 1" > x_div_y_1
```
