# C++ library for the gated cytometry data

# License
Copyright 2019, Fred Hutchinson Cancer Research Center
See the included LICENSE file for details on the license granted to the user of this software.

`cytolib` provides the c++ library for users to use and interact with the `GatingSet` (the gated cytometry data structure) at c++ level.


### Reporting Bugs or Issues
- Use the issue template in github when creating a new issue. 
- Follow the instructions in the template (do your background reading).
- Search and verify that the issue hasn't already been addressed.
- Check the Bioconductor support site. 
- Make sure your flow packages are up to date.
- THEN if your issue persists, file a bug report.

Otherwise, we will close your issue without responding.

## Installation as a R package
The **cytolib** package is installed via `R CMD INSTALL ...`. 

R packages wishing to use the libraries in `cytolib` need to:

- add `cytolib` to **LinkingTo** field in the **DESCRIPTION** file so the compiler knows where to find the headers when the user package is complied
e.g.

```
LinkingTo: cytolib
```
See **CytoML** package for the example of using `cytolib`.

## Installation as a C++ standalone library

**System requirement**
1. cmake
2. g++ (>=4.9) or clang++(>= 7.0.1)
3. libblas, liblapack, ZLIB, boost c++ library

**Installation**

```bash
# enter your project directory
$ cd cytolib

# it is always a good idea to not pollute the source with build files
# so create a new build directory
$ mkdir build
$ cd build

# run cmake to configure the package for your system
$ cmake ..

# to select different compiler other than the default
# e.g. `cmake -DCMAKE_CXX_COMPILER=clang++` 

#To install the library to custom directory, use `-DCMAKE_INSTALL_PREFIX` option
# e.g. `cmake -DCMAKE_INSTALL_PREFIX=/usr/local` 
   
$ make

#to install the package
$ make install

```
   
