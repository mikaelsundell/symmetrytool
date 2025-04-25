Symmetrytool
==================

[![License](https://img.shields.io/badge/license-BSD%203--Clause-blue.svg?style=flat-square)](https://github.com/mikaelsundell/logctool/blob/master/README.md)

Introduction
------------

Symmetrytool is a utility for exploring the math of symmetry in art and design.

![Sample image or figure.](images/image.png 'symmetrytool')


Usage
-----

Print symmetrytool help message with flag ```--help```.

```shell
symmetrytool -- a utility for creating symmetry images

Usage: symmetrytool [options] ...

General flags:
    --help                     Print help message
    -v                         Verbose status messages
    -d                         Debug status messages
Input flags:
    --centerpoint              Use centerpoint for symmetry
    --symmetrygrid             Use symmetry grid for symmetry
    --label                    Use label for symmetry
    --aspectratio ASPECTRATIO  Set aspectratio (default:1.5)
    --scale SCALE              Set scale (default: 0.5)
    --color COLOR              Set color (default: 1.0, 1.0, 1.0)
    --size SIZE                Set size (default: 1024, 1024)
Output flags:
    --outputfile OUTPUTFILE    Set output file
```

Generate aspect ratio 1.5 symmetry grid  in OpenEXR float
--------

```shell
./symmetrytool --aspectratio 1.5 --outputfile ./symmetrytool_1.5.png --symmetrygrid --centerpoint --size 1500,1000 -v -d --scale 1
```

Download symmetry grids for aspectratios charts
-------------

LogC charts are available EXR float and DPX 10-bit precision, EI 800.


| Aspect ratio     | Output type | Download
| ----------- | ----------- | ----------- |
| 1.5 | ```./symmetrytool --aspectratio 1.5 --outputfile ./symmetrytool_1.5.png --symmetrygrid --centerpoint --size 1500,1000 -v -d --scale 1```  | x1.5 [PNG](https://mikaelsundell.s3.eu-west-1.amazonaws.com/github/symmetrytool/symmetrytool_1.5.png) |
| 1.78 | ```./symmetrytool --aspectratio 1.78 --outputfile ./symmetrytool_1.78.png --symmetrygrid --centerpoint --size 1780,1000 -v -d --scale 1```  | x1.78 [PNG](https://mikaelsundell.s3.eu-west-1.amazonaws.com/github/symmetrytool/symmetrytool_1.78.png) |
| 1.85 | ```./symmetrytool --aspectratio 1.85 --outputfile ./symmetrytool_1.85.png --symmetrygrid --centerpoint --size 1850,1000 -v -d --scale 1```  | x1.85 [PNG](https://mikaelsundell.s3.eu-west-1.amazonaws.com/github/symmetrytool/symmetrytool_1.85.png) |
| 2.0 | ```./symmetrytool --aspectratio 2.0 --outputfile ./symmetrytool_2.0.png --symmetrygrid --centerpoint --size 2200,1000 -v -d --scale 1```  | x2.0 [PNG](https://mikaelsundell.s3.eu-west-1.amazonaws.com/github/symmetrytool/symmetrytool_2.0.png) |
| 2.20 | ```./symmetrytool --aspectratio 2.20 --outputfile ./symmetrytool_2.20.png --symmetrygrid --centerpoint --size 2200,1000 -v -d --scale 1```  | x2.20 [PNG](https://mikaelsundell.s3.eu-west-1.amazonaws.com/github/symmetrytool/symmetrytool_2.20.png) |
| 2.35 | ```./symmetrytool --aspectratio 2.35 --outputfile ./symmetrytool_2.35.png --symmetrygrid --centerpoint --size 2350,1000 -v -d --scale 1```  | x2.35 [PNG](https://mikaelsundell.s3.eu-west-1.amazonaws.com/github/symmetrytool/symmetrytool_2.35.png) |
| 2.39 | ```./symmetrytool --aspectratio 2.39 --outputfile ./symmetrytool_2.39.png --symmetrygrid --centerpoint --size 2390,1000 -v -d --scale 1```  | x2.39 [PNG](https://mikaelsundell.s3.eu-west-1.amazonaws.com/github/symmetrytool/symmetrytool_2.35.png) |

Building
--------

The symmetrytool app can be built both from commandline or using optional Xcode `-GXcode`.

```shell
mkdir build
cd build
cmake .. -DCMAKE_MODULE_PATH=<path>/modules -GXcode
cmake --build . --config Release -j 8
```

**Example using 3rdparty on arm64 with Xcode**

```shell
mkdir build
cd build
cmake ..
cmake .. -DCMAKE_MODULE_PATH=<path>/modules -DCMAKE_PREFIX_PATH=<path>/3rdparty/build/macosx/arm64.debug -GXcode
```

Download
---------

Symmetrytool is included as part of pipeline tools. You can download it from the releases page:

* https://github.com/mikaelsundell/pipeline/releases

Dependencies
-------------

| Project     | Description |
| ----------- | ----------- |
| Imath       | [Imath project @ Github](https://github.com/AcademySoftwareFoundation/Imath)
| OpenImageIO | [OpenImageIO project @ Github](https://github.com/OpenImageIO/oiio)
| 3rdparty    | [3rdparty project containing all dependencies @ Github](https://github.com/mikaelsundell/3rdparty)

Project
-------------

* GitHub page   
https://github.com/mikaelsundell/symmetrytool
* Issues   
https://github.com/mikaelsundell/symmetrytool/issues


Resources
---------

* Dynamic Symmetry: The Foundation of Masterful Art   
Author: Tavis Leaf Glover

Copyright
---------

* Roboto font   
https://fonts.google.com/specimen/Roboto   
Designed by Christian Robertson
