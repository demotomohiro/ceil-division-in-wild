# OpenSSL

From:
https://www.openssl.org
https://github.com/openssl/openssl

## Commands to get a list of lines that do ceil division

```
git clone --depth 1 https://github.com/openssl/openssl.git
cd openssl
git grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+ - 1\) / [[:alnum:]_.]+" > x_y-1_div_y
```
