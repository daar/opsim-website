---
title: 'Monthly update August, 2016'
media_order: OpSim_update.png
published: true
date: '25-08-2016 00:00'
publish_date: '25-08-2016 00:00'
metadata:
    author: admin
taxonomy:
    category:
        - General
slug: monthly-update-august-2016
visible: true
header_image: '1'
header_image_file: OpSim_update.png
summary:
    enabled: '1'
    format: short
    size: 128
author: admin
---

Hi all! Here’s the second monthly update on OpSim and it’s development. Unfortunately there was no time for me in May, June and July to write up an update, but that means that I have more to share this time!  
In total 28 commits were made over the last three months. This does not sound impressive, but it has involved a lot of work on different area’s of the project, ranging from a new build system to the beginnings of a new UI!  
Please note that we are always welcoming people that would like to join this project! Even if your contribution is small or limited to a specific area, feel free to join our team.  
Here’s a recap of the work done during May, June and July.

**Website / communication**
- A .cc domain has been registered for the OpSim project ([www.opsim.cc](http://www.opsim.cc/)). For now the domain will forward to the SourceForge website. We would like to host our own site and collaboration tools and are looking for someone that is able to sponsor/facilitate us. Please [contact me](mailto://darius@opsim.cc) if you can help.
- Source documenting software is now definitely chosen to be [pasdoc](https://sourceforge.net/projects/pasdoc/?source=directory). The documentation has been updated to represent the current state of the software and uploaded to the site. Additionally a tool has been made to help with documenting the sources. When run it automatically creates placeholder comments.
- The first three sections (`About` / `Coding standards` and `Setting up the environment`) of the Developers handbook have been rewritten. The contents is now more practical and more in line with the current state.
- The Users handbook has been updated with the implemented physical properties methods.
- We are in need of a maintainer for the documentation, someone that would like to reorganize everything we have and rewrite were needed.

**Development**
- Implemented a [new build system called FMake](http://opsim.sourceforge.net/?p=125) for the OpSim modules and test applications. In time the complete compilation, installing and releasing of OpSim will be moved to FMake. All new software that is merged to trunk will be supported by FMake.
- A basic working [user interface](http://opsim.sourceforge.net/?p=130) for OpSim has been created. Contrary to the current code-base, the new GUI will be [OpenGL](https://www.opengl.org/) based. The interface will be non-blocking, non-overlapping and non-modal. In the coming weeks a preliminary version will committed to trunk, after which the implementation of the different `space types` can be implemented.
- The [physical properties library](http://opsim.sourceforge.net/?p=89) has been merged with trunk. The new library handles a wide range of different property models. In this first merge in total 57 components were uploaded as a start. We are seeking for volunteers that like to add more models and components to our database.

**Plans and todos**
- Started work on a graphical physical property editor. For fast prototyping the editor will be implemented in Lazarus, later, once the application will work as intended and the OpSim UI is committed, the code will be merged into the new OpSim UI.
- Python support is being tested in branches. No conclusion yet on how this might work technically and practically.
- Simulation solver engine work has begun in branches. However this is a complex task and needs a lot of extra work and help.
- Work is planned to create a “custom” binary file format for OpSim. Main features for this file format are: fast saving of data, platform and architecture independent, easily extendible (if possible automatic serialization for saving of data) and upward/downward compatibility.

-Darius-