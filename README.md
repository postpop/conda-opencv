conda-opencv
============

see original [README.MD](https://github.com/menpo/conda-opencv)

ONLY TESTED ON OSX!!

For this to work, you first need to install FFMPEG (<v.3.0) via [homebrew](http://brew.sh) on OSX:
```
brew install https://raw.githubusercontent.com/Homebrew/homebrew/b42854ae8085fb60ff72a47021a683373ed97e7b/Library/Formula/ffmpeg.rb
```
To prevent brew from upgrading FFMPEG to the newest version: `brew pin ffmpeg`.

Then build opencv:
```
conda install conda-build
git clone https://github.com/postpop/conda-opencv
cd conda-opencv 
conda build conda/
conda install /PATH/TO/OPENCV/PACKAGE.tar.gz
```
