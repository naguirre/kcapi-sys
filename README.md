# The Raw Rust Bindings for libkcapi

![CI Badge](https://github.com/puru1761/libkcapi-sys/actions/workflows/main.yml/badge.svg)

This repository contains the official raw low-level bindings for
[libkcapi](https://github.com/smuellerDD/libkcapi/). *DO NOT* use these
bindings directly in your project. Instead, a safe Rusty API will be provided
as a part of the `libkcapi-rs` crate.

## Pre-requisites

Prior to building this project, clone this repository, and also checkout
all it's included submodules recursively.

```
git clone https://github.com/puru1761/libkcapi-sys.git --recurse-submodules
```

Install all build dependencies. These are:

* `autotools`
* `autoconf`
* `llvm-dev`

### RPM based package manager

```
sudo yum install automake autoconf llvm-devel
```

### Debian based package manager

```
sudo apt-get install autotools-dev autoconf llvm-dev
```

If `LLVM_CONFIG_PATH` is not set, then set it with:

```
export LLVM_CONFIG_PATH="/path/to/llvm-config"
```

## Build

We use cargo as our build system for building this crate. Build it using:

```
cargo build
```

## Test

We have a few sanity tests written to make sure that the bindings work
as expected. Run these tests using:

```
cargo test
```

## Author

* Purushottam A. Kulkarni <<puruk@protonmail.com>>