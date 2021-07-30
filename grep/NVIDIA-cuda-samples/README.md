# CUDA Samples

From:
https://github.com/NVIDIA/cuda-samples

Most of ceil division in this project is used to get number of thread blocks from number of input data and number of threads per block.

## Commands to get a list of lines that do ceil division

```
git clone --depth 1 https://github.com/NVIDIA/cuda-samples.git
cd cuda-samples
git grep -E "\([[:alnum:]_.]+ \+ [[:alnum:]_.]+ - 1\) / [[:alnum:]_.]+" > x_y-1_div_y
git grep -E "\([[:alnum:]_.]+ / [[:alnum:]_.]+\) \+ 1" > x_div_y_1
```
