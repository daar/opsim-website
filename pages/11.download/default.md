---
title: Download
published: true
date: '23-03-2016 00:00'
publish_date: '23-03-2016 00:00'
metadata:
    author: darius
slug: download
process:
    markdown: true
    twig: true
visible: false
github: true
summary:
    enabled: true
    format: short
    size: 128
author:
    name: darius
---

OpSim is still under active development and no stable release has yet been released. In the future there will be releases for Windows, Linux and Mac OS.

<i class="fa fa-windows fa-2x"></i>
<i class="fa fa-linux fa-2x"></i>
<i class="fa fa-apple fa-2x"></i>
<i class="fa fa-file-archive-o fa-2x"></i>

OpSim is [Free & Open Source Software](../license/).

## OpSim release 0.01

This is just a prototype release. It is intended to provide a current view of the development effort even for those community members who did not managed to setup a development environment on their computers. Please understand that what you are seeing is only the user interface.  The majority of the work on OpSim has gone into the infrastructure that cannot be seen here.

All that is needed for the Windows operating system is inside the ZIP file. The main executables are:
- OpSim.exe: is the simulator itself.
- OpSimTest.exe: a collection of unit tests for several classes in the source code.
- FlashTest.exe: an application being used in the development and testing of the fundamental flash routines.

What we have so far:
- A basic GUI with a Process Flow sheet Designer (PFD).
- A pallet with a few unit operations. The drag-drop functionality already working.
- A pure component database properly structured.
- A database inspector.
- A growing collection of classes for thermodynamic, solver, etc.

- [**OpSim-0.0.1-win32.zip** 4.45 MB 17 downloads](https://github.com/daar/opsim/releases/download/0.01/OpSim-0.0.1-win32.zip)
- [**Source code**](https://github.com/daar/opsim/archive/0.01.zip)