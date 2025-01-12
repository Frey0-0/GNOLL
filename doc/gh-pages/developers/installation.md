---
title: Setup
parent: Technical Information
published: true
nav_order: 0
---

# Setup
## OS Information

- Linux - Tested on Ubuntu '18.
- Windows - Tested on Windows Subsystem for Linux (WSL)
- Mac - Untested.

## Common Pre-requisites
```bash
sudo apt-get install bison flex make python3-pip -y
```

## C/C++
```bash
make all
```

## Go
```bash
make go
```

## Python
Available from [PyPi](https://pypi.org/project/gnoll/)
```bash
pip install gnoll
```
If you are running from sourcecode:
```bash
make python
```

## Perl
```bash
make perl
```

## JavaScript Setup

### Pre-Requisites
```bash
sudo apt-get install emscripten nodejs
```

### Build
```bash
make javascript
```

### Run
```bash
node a.out.js
```

## Something Else?
### SWIG
The swig bindings are already generated for you in `src/swig/gnoll.i`. Follow the specific instructions in the SWIG documentation to build your own binding.
Note: The current bindings do not return a result directly - You should read from the file that is generated.

### Shared Library
Many languages allow importing of code via shared object. You can find this .o file in the build folder after running `make all`
