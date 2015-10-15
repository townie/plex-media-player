# How-To build Qt 5.5.0 on Windows
This procedure was ran on a freshly installed Win7 64 bits.

This procedure assumes that the build root is `C:\qt\` but it can be changed in the beginning of each `.bat` file

1. Install Visual Studio 2013
- Install [Visual Studio 2013 Update 4](http://www.microsoft.com/fr-fr/download/details.aspx?id=44921) 
- Install [Windows SDK 8](https://msdn.microsoft.com/en-us/windows/desktop/hh852363.aspx)
- Install [ActivePerl](http://www.activestate.com/activeperl/downloads)
- Install [Python 2.7.10](https://www.python.org/downloads/release/python-2710)
- Install the following gnutools:
  - [Bison](http://gnuwin32.sourceforge.net/downlinks/bison.php)
  - [GPerf](http://gnuwin32.sourceforge.net/downlinks/gperf.php)
  - [Flex](http://gnuwin32.sourceforge.net/downlinks/flex.php)
- Grab [ICU sources](http://download.icu-project.org/files/icu4c/55.1/icu4c-55_1-src.zip) and unpack them in `C:\qt\icu`
- Grab [Openssl 1.0.2d](https://www.openssl.org/source/) and unpack them in `C:\qt\openssl`
- Grab [Qt Sources](http://download.qt.io/official_releases/qt/5.5/5.5.0/single/qt-everywhere-opensource-src-5.5.0.zip) and unpack them in  `C:\qt\qt5`
- drop the three `.bat` files in the steps below in `C:\qt\` 
- Open `C:\qt\icu\source\allionone\allinone.sln` with VS2013, you will be prompted for project conversion. Once the project is converted, just close it.
- run `c:\qt\buildicu.bat`
- run `c:\qt\buildopenssl.bat`
- run `c:\qt\buildqt.bat`

The qt build will land in `C:\qt\qt5\build`


# buildicu.bat
```
set BUILD_ROOT=C:\qt
cd ..
```

# buildopenssl.bat
```
set BUILD_ROOT=C:\qt
```

# buildqt.bat
```
set BUILD_ROOT=C:\qt
```