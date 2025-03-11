CUDA 12.1 with gcc 12.3

# CUDA inside conda

`
conda install cuda -c nvidia/label/cuda-12.1.0
`

# modifying gcc
`
which g++
`
should point to conda env bin

else follow this

```
conda install -c conda-forge gxx_linux-64=12.3.0
ln -sf $CONDA_PREFIX/bin/x86_64-conda-linux-gnu-g++ $CONDA_PREFIX/bin/g++ #symbolic links
$CONDA_PREFIX/bin/g++ --version #check
export PATH=$CONDA_PREFIX/bin:$PATH #include the path
```
