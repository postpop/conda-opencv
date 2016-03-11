conda-opencv
============
This repository contains a conda recipe for automatically building the OpenCV Python package and uploading it to our anaconda repository, menpo. This recipe provides builds for Win32, Win64, OSX64 and Linux64 (Ubuntu 12.04 and above). **Due to limitations of OpenCV, only Python 2.7 is supported**.

ONLY TESTED ON OSX!!

Build Settings
--------------
The following OpenCV functionality is **disabled or unavailable** for the automated builds:

  - world
  - androidcamera 
  - dynamicuda
  - java 
  - ocl
  - viz
  - Video I/O (including FFMPEG)
  - OpenNI
  - Cuda
  - OpenCL
  - IPP
  - Concurrency
  - C=

**Specific to Linux**
  - **GUI:** Built with GTK+ 2.x and GThread

Install FFMPEG (<v.3.0) via homebrew on OSX:
```
brew install https://raw.githubusercontent.com/Homebrew/homebrew/b42854ae8085fb60ff72a47021a683373ed97e7b/Library/Formula/ffmpeg.rb
```
Then build opencv:
```
conda install conda-build
git clone https://github.com/menpo/conda-opencv
cd conda-opencv 
conda build conda/
conda install /PATH/TO/OPENCV/PACKAGE.tar.gz
```
