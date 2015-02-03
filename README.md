# OCR-with-KMeans
optical character recognition with K means
Readme
======

Installation for Linux/Ubuntu.

Pre-req to run the application
=====================================
Installing softwares needed(Python, numpy, OpenCV)
Python on Ubuntu 14.04
======================
Install dependencies:
$ sudo apt-get install python-software-properties
Add the repo:
$ sudo add-apt-repository ppa:fkrull/deadsnakes
Update the repo index:
$ sudo apt-get update
Install Python 3.3:
$ sudo apt-get install python3.3
Adding numpy:
apt-get install python-numpy

OpenCV 2.4 on Ubuntu 14.04
==========================
Ubuntu 12.04 provides a package of OpenCV 2.3.1:
$ sudo apt-get install libopencv-dev
Libraries and tools required by OpenCV:
$ sudo apt-get install build-essential checkinstall cmake pkg-config yasm
Libraries for reading and writing various image types:
$ sudo apt-get install libtiff4-dev libjpeg-dev libjasper-dev
To add video capturing/encoding/decoding capabilities to the highgui module:
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libdc1394-22-dev libxine-dev libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev libv4l-dev
Packages needed to build the Python wrappers:
$ sudo apt-get install python-dev python-numpy
Install Intel TBB to enable parallel code in OpenCV:
$ sudo apt-get install libtbb-dev
Download OpenCV:
http://sourceforge.net/projects/opencvlibrary/files/opencv-unix/2.4.0/OpenCV-2.4.0.tar.bz2/download
$ tar -xvf OpenCV-2.4.0.tar.bz2
$ cd OpenCV-2.4.0/
$ mkdir build
$ cd build
Configure using CMake
$ cmake -D WITH_QT=ON -D WITH_XINE=ON -D WITH_OPENGL=ON -D WITH_TBB=ON -D BUILD_EXAMPLES=ON ..
Compile:
$ make
Install
$ sudo make install
Edit /etc/ld.so.conf and add line /usr/local/lib in the end.
configure dynamic linker run-time bindings
$ sudo ldconfig


Running the program:
===================
to preprecess the data:
$ python preprocessing.py
Enter the Input File:<enter one of the file from data_set folder>
$ python trainAndtest.py
$ python run.py
















