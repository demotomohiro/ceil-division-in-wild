# Linux kernel source

From:
https://www.kernel.org

There are many ceil division in linux kernel.
`DIV_ROUND_UP` / `__KERNEL_DIV_ROUND_UP` macro is used for ceil division.

In `linux-5.13.6/include/linux/math.h`:
```c
#define DIV_ROUND_UP __KERNEL_DIV_ROUND_UP
```

linux-5.13.6/include/uapi/linux/const.h
```c
#define __KERNEL_DIV_ROUND_UP(n, d) (((n) + (d) - 1) / (d))
```

linux-5.13.6/tools/include/linux/kernel.h 
```c
#define DIV_ROUND_UP(n,d) (((n) + (d) - 1) / (d))
```

## Commands to get a list of lines that do ceil division

```
wget https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.13.6.tar.xz
tar xf linux-5.13.6.tar.xz
cd linux-5.13.6

grep "DIV_ROUND_UP" -r linux-5.13.6 > DIV_ROUND_UP
grep "__KERNEL_DIV_ROUND_UP" -r linux-5.13.6 > __KERNEL_DIV_ROUND_UP
grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+ - 1\) / [[:alnum:]_.]+" -r linux-5.13.6 > x_y-1_div_y
grep -E "\([[:alnum:]_.]+ >> [[:digit:]]+\) \+ \(\(?[[:alnum:]_.]+ & [[:digit:]]+\)?" -r linux-5.13.6 > x_shr_y_plus_x_and_z
```

Uncompressing the file on MS Windows might fail as there is a file "aux.c" and that file name cannot be used on MS Windows.
