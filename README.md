# Macau-cpp - Bayesian Factorization with Side Information
Macau is highly optimized and parallelized implementation of Bayesian Factorization.

Macau trains a Bayesian model for **collaborative filtering** by also incorporating side information on rows and/or columns to improve the accuracy of the predictions.
Macau employs Gibbs sampling to sample both the latent vectors and the link matrix that connects the side information to the latent vectors. Macau supports **high-dimensional** side information (e.g., millions of features) by using **conjugate gradient** based noise injection sampler.

# Examples
For examples see [documentation](http://macau.readthedocs.io/en/latest/source/examples.html).

# Installation
To install Macau it possible to use pre-compiled binaries or compile it from source.

## Source installation on Ubuntu
```bash
# install dependencies:
sudo apt-get install python-pip python-numpy python-scipy python-pandas cython
sudo apt-get install libopenblas-dev autoconf gfortran

# checkout and install Macau
git clone --recursive https://github.com/jaak-s/macau.git
cd macau
python setup.py install --user
```

## Source installation on any Linux
Make sure that `pip` is available and OpenBLAS or some other BLAS is installed.
Then install following packages using pip: `numpy scipy pandas cython`, e.g. by
```
# skip any of them if already available
pip install numpy --user
pip install scipy --user
pip install pandas --user
pip install cython --user

# checkout and install Macau
git clone https://github.com/jaak-s/macau.git
cd macau
python setup.py install --user
```

## Source installation on Mac
```bash
# install dependencies
pip install numpy
pip install scipy
pip install pandas
pip install cython
# install brew (http://brew.sh/)
brew install homebrew/science/openblas
brew install gcc

# checkout and install Macau
git clone --recursive https://github.com/jaak-s/macau.git
cd macau
CC=g++-5 CXX=g++-5 python setup.py install
```

## Binary installion on Ubuntu
There is a plan to support Python wheel packages. Currently, we do not have one built yet.

# Contributors
- Jaak Simm (Macau C++ version, Cython wrapper, Macau MPI version)
- Tom Vander Aa (OpenMP optimized BPMF)
- Tom Haber (Original BPMF code)

