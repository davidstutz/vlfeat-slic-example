# Using VLFeat's SLIC from C++

This project is a simple example of how to use [VLFeat](http://www.vlfeat.org/)'s "Simple Linear Iterative Clustering" (SLIC) implementaiton from C++.

The algorithm is desribed in detail in [1].

[1] R. Achanta, A. Shaji, K. Smith, A. Lucchi, P. Fua, S. Süusstrunk. SLIC Superpixels. Technical
report, EPFL, Lausanne, 2010.

Have a look at my blog article ybout VLFeat's SLIC implementation: [http://davidstutz.de/running-vlfeats-slic-superpixels-using-cmake-c/](http://davidstutz.de/running-vlfeats-slic-superpixels-using-cmake-c/)

## Requirements

* Build essentials: `sudo apt-get install build-essential`
* CMake: `sudo apt-get install cmake`
* OpenCV: [http://docs.opencv.org/doc/tutorials/introduction/linux_install/linux_install.html#linux-installation](http://docs.opencv.org/doc/tutorials/introduction/linux_install/linux_install.html#linux-installation)

## Usage

    $ git clone https://github.com/davidstutz/vlfeat-slic-example.git
    $ cd vlfeat-slic-example
    $ cmake .
    $ make
    [ 20%] Building C object CMakeFiles/vlfeat_slic.dir/lib_vlfeat/vl/host.c.o
    [ 40%] Building C object CMakeFiles/vlfeat_slic.dir/lib_vlfeat/vl/random.c.o
    [ 60%] Building C object CMakeFiles/vlfeat_slic.dir/lib_vlfeat/vl/generic.c.o
    [ 80%] Building C object CMakeFiles/vlfeat_slic.dir/lib_vlfeat/vl/slic.c.o
    Linking C static library libvlfeat_slic.a
    [ 80%] Built target vlfeat_slic
    Scanning dependencies of target vlfeat_slic_example
    [100%] Building CXX object vlfeat_slic_cli/CMakeFiles/vlfeat_slic_example.dir/main.cpp.o
    Linking CXX executable ../bin/vlfeat_slic_example
    [100%] Built target vlfeat_slic_example
    $ ./bin/vlfeat_slic_example
    
Make sure that `Lenna.png` is present in the root directory (or the directory from where you are running `vlfeat_slic_example`).

## Result

![Superpixel segmentation of `Lenna.png`.](Lenna_contours.png?raw=true "Superpixel segmentation of `Lenna.png`.")

# License

VLFeat is distributed under the BSD license, see [https://github.com/vlfeat/vlfeat](https://github.com/vlfeat/vlfeat).

For license details of `Lenna.png`, see [http://en.wikipedia.org/wiki/Lenna#mediaviewer/File:Lenna.png](http://en.wikipedia.org/wiki/Lenna#mediaviewer/File:Lenna.png).

Copyright 2014 David Stutz

The application is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

The application is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

See http://www.gnu.org/licenses/.