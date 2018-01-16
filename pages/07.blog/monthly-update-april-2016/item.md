---
title: 'Monthly update April, 2016'
media_order: OpSim_update.png
published: true
date: '27-04-2016 00:00'
publish_date: '27-04-2016 00:00'
metadata:
    author: admin
taxonomy:
    category:
        - General
slug: monthly-update-april-2016
visible: true
header_image: '1'
header_image_file: OpSim_update.png
summary:
    enabled: '1'
    format: short
    size: 128
author: admin
---

Hi all! This is the first of hopefully many monthly updates on the development of OpSim. The updates will be posted on the website and forwarded to the mailing lists and forum around the end/beginning of each month.  
 The first commit after more than 8 years was done again on march 23rd 2016. Since this commit a lot of work has been done and quite some plans have been made. Please note that we are always welcoming people that would like to join this project! Even if your contribution is small or limited to a specific area, feel free to join our team.  
 Here’s a recap of the work done over the previous month.

**Website / communication**
- A website has been created on the SourceForge web server. It does not function fully as SourceForge blocks some features, but for now it’s more than sufficient. We’re looking for someone that would like to take up the (currently small) task of running and maintaining the site.
- New [mailing lists](https://sourceforge.net/p/opsim/mailman/?source=navbar) have been created on SourceForge for users, developers and the core team.
- Documentation has been ported from different formats like Open Office and MS Office to [restructuredText](http://docutils.sourceforge.net/rst.html). There’s a user manual and developers manual. We’re in need of a maintainer for the documentation, it’s pretty messy for now, but it works. The documentation is stored in SVN.
- Made a start with source documenting. Currently [doxygen ](http://www.stack.nl/~dimitri/doxygen/)and [pasdoc ](https://sourceforge.net/projects/pasdoc/?source=directory)have been investigated. While doxygen seems to be a better and more complete tool, it needs a pre-processor called [pas2dox](https://sourceforge.net/projects/pas2dox/). Needs more work on.
- An OpSim logo has been defined and agreed upon!

**Development**
- Fixed compilation of trunk with FPC 2.6.4 and up.
- Implemented a stand alone chemical formula parser in trunk
- Implemented a unit converter in trunk
- Quite some work in the opsim_darius branch (see `plans`)
- Localization has been tested in branches and a proper working solution has been found. Will be used for trunk.
- The internals of OpSim will be implemented with a minimal use of classes. Not that classes will be completely forbidden, however tests on different platforms and architectures show that records use a lot less resources and are faster executed. For a heavy simulation environment this is important. A linked list unit has been added to trunk help with creating and managing data structures more easily.

**Plans and todos**
- In branches there’s a library called physprops. The library currently supports a number of models and components, but needs more work on before committing to trunk. The component definitions are stored in [JSON](http://www.json.org/) format.
- OpSim is in need of a build system to assist in generating source files and building them in the correct order. Tests have been done with fpmake and cmake. No conclusions drawn yet.
- Python support has been tested in branches. No conclusion yet on how this might work technically and practically.
- Simulation solver engine work has begun in branches. However this is a complex task and needs a lot of extra work and help.
- First work has started on the new user interface for OpSim. Contrary to the current codebase, the new GUI will be [OpenGL](https://www.opengl.org/) based. The interface will be non-blocking, non-overlapping and non-modal. More details to follow as soon as other items are finalized and merged to trunk.
- Work is planned to create a “custom” binary file format for OpSim. Main features for this file format are: fast saving of data, platform and architecture independent, easily extendible (if possible automatic serialization for saving of data) and upward/downward compatibility.

-Darius-