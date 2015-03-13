# On Linux #

This is how I do it on my 64bit Kubuntu 8.04:

  1. Make sure you have required packages installed. You need to install qt-4 development packages. All non-standard dependencies are included into source distribution (including Box12D itself). Also - at least until first release - you need Subversion client to get the source.
  1. get the source, in a way suggested by google's hosting page:
```
  svn checkout http://flyer2d.googlecode.com/svn/trunk/ flyer2d
```
  1. Get into source directory, generate make file and build it:
```
  cd flyer2d
  qmake-qt4 flyer.pro
  make -k
```
> If you get some linking errors - just run make again - sometimes it tries to build executable before required library.
  1. If everything goes OK, you should have compiled binaries in fyler (and editor) sub directories.
```
  ./flyer/flyer
```

You need to have hardware OpenGL implementation go get this working with decent speed.

# On Windows #

You can get easy-to-install Windows Qt package from this site: http://trolltech.com/developer/downloads/qt/windows , which also installs MinGW (GNU compiler and tools for windows).

Once you get Qt and MinGW installed, building instructions are identical like for Linux (see previous chapter). You only have to use 'MinGW/Qt console' available from Qt's start-menu directory, and probably simply use 'qmake' instead of 'qmake-qt4' for configuration.