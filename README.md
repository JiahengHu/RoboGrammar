# RoboGrammar

This repo is adopted from \[[RoboGrammar](https://github.com/allanzhao/RoboGrammar.git)\] with modification, used for CoRL 22 submission on GLSO.


## Prerequisites

Commands were tested on Ubuntu 18.04.

[CMake](https://cmake.org/download/) >= 3.8
* Check with `cmake --version`

GLEW
* `sudo apt-get install libglew-dev`

Python 3.6 or later + headers
* Check the Python version with `python3 —-version`. If new enough, install Python headers: `sudo apt-get install python3-dev`
* Otherwise, install the latest version of both: `sudo apt-get install python3.9 python3.9-dev`

Note: Newer versions of Python may be available through the "deadsnakes" PPA:

```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get update
```

## Building (Linux, Mac OS)

`git clone https://github.com/allanzhao/RoboGrammar.git`

`cd RoboGrammar`

`git submodule update --init`

`mkdir build; cd build`

`cmake -DCMAKE_BUILD_TYPE=RelWithDebInfo ..`

`make -j8` (replace 8 with the number of CPU cores available)

## Installing Python Packages

Make sure you are in the `RoboGrammar` directory.


`python3 examples/design_search/setup.py develop`

`python3 build/examples/python_bindings/setup.py develop`

```
pip3 install numpy-quaternion
```

