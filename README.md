# caffe-notes

## build caffe on ubuntu 16.04

### fetch caffe source code

```bash
git clone https://github.com/BVLC/caffe.git
```

### install dependency libraries

```bash
sudo apt install libprotobuf-dev libleveldb-dev libsnappy-dev libopencv-dev libhdf5-serial-dev protobuf-compiler

sudo apt install --no-install-recommends libboost-all-dev

sudo apt install libopenblas-dev

sudo apt install libatlas-base-dev
```

In your Makefile.config try to append **/usr/include/hdf5/serial/** to INCLUDE_DIRS:

### compilation with make

```bash
cp Makefile.config.example Makefile.config
# Adjust Makefile.config (for example, if using Anaconda Python, or if cuDNN is desired)
make all
make test
make runtest
```

### reference

https://github.com/BVLC/caffe

http://caffe.berkeleyvision.org/installation.html#compilation
