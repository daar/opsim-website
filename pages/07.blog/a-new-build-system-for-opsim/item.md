---
title: 'A new build system for OpSim'
media_order: fmake.png
published: true
date: '08-08-2016 00:00'
publish_date: '08-08-2016 00:00'
metadata:
    author: admin
taxonomy:
    category:
        - Coding
        - Planning
slug: a-new-build-system-for-opsim
visible: true
header_image: '1'
header_image_file: fmake.png
summary:
    enabled: '1'
    format: short
    size: 128
author: admin
---

Here’s a post about the new build system called [FMake](http://daar.github.io/pmake/) that has been developed for OpSim. Until now OpSim was a [Lazarus ](http://www.lazarus-ide.org/)project with a Lazarus project file. However, over the last weeks (and still some planned), FPC only libraries have been added to trunk. Looking forward tells us that OpSim will need a build system some day eventually.  
  
 The new build system FMake is much more flexible compared to Lazarus project files. Sure one can setup a debug or release compile mode in Lazarus, but as each executable is it’s own project, one will need to manage this per project file. This will become even more work when more libraries and program files will be added to the code base. A build system allows to add global and local options more easily, it assists with creating binary releases and installing software to production systems as well as assisting with running tests. For now FMake does not yet support all functionality yet, but once it is needed it can be added of course.

**Alternatives**  
 Of course the alternatives were investigated as well. Here are some of them known to the FPC community.

[FPCMake ](http://wiki.freepascal.org/Fpcmake)This tool is supplied by the FPC developers. It was originally the main build tool for the FPC compiler. FPCMake will generate Make files from Makefile.fpc files. Similar to Make, FPCMake are relatively complex to use. It requires a deeper understanding of Make.

[FPMake](http://wiki.freepascal.org/FPMake) This tool is the successor of FPCMake. Instead of generating Make files it can be compiled into a fpmake executable. FPMake is a powerful tool which is currently used for building the FPC compiler as well as the Lazarus IDE. Even though the approach is different from FPCMake, FPMake is still considered a difficult tool to be used. To be able to compile independent packages, fpmake.pp files are scattered across the source tree with a lot of conditional defines in them.

Apart from the two mentioned above there are other alternatives like the good old Make, WANT, and CMake. CMake is originally a build system written in python for C compilers out of the box. There are also [modules](https://github.com/daar/CMake4Pascal) for CMake to allow FPC project to be built. However testing these modules showed that there are still some issues to be resolved before CMake becomes a mature solution.

**About FMake**  
 Fmake is functionally very similar to CMake. Just like CMake FMake requires FMake.txt files to be placed in the source tree that define libraries, programs, install and custom commands on a package basis. FMake will concatenate all the FMake.txt files, which is valid pascal code and compile it into a single make executable. Once created, the developer can build the whole source by issuing a make command. The sources are split up logically into packages. These packages are containers of commands that belong functionally to each other.

FMake is not completely ready yet, but the current code base is fully functional and can be used. Hopefully in the future more people will get enthusiastic about this new build tool and will start supporting it. The GitHub site contains more information on FMake, together with a comprehensive manual and an issue list.