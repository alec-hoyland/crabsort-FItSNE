# crabsort-FItSNE
This is a plugin for [crabsort](https://github.com/sg-s/crabsort)

It implements fast Fourier transform-interpolated t-distributed stochastic neighborhood embedding,
a type of dimensionality-reduction algorithm.

For more information, see:
https://github.com/KlugerLab/FIt-SNE
or the paper by Linderman & Steinerberger at https://arxiv.org/abs/1711.04712

## Installation
FIt-SNE requires a separate repository.

### macOS & GNU/Linux
1. Download the repository from: https://github.com/KlugerLab/FIt-SNE
 or clone using
 ```
   $ git clone https://github.com/KlugerLab/FIt-SNE
```
2. Add the downloaded folder to your MATLAB path
 ```
    >> addpath path/to/FIt-SNE`
    >> savepath
 ```
3. Download FFTW from http://www.fftw.org/ or get it for your operating system/distribution
4. From the root directory of FIt-SNE, run:
 ```
   $ g++ -std=c++11 -O3  src/sptree.cpp src/tsne.cpp src/nbodyfft.cpp  -o bin/fast_tsne -pthread -lfftw3 -lm
 ```

### Windows
Follow steps 1 and 2 above,
then go to https://github.com/KlugerLab/FIt-SNE and download the compiled binary instead.
