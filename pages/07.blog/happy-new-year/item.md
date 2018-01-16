---
title: 'Happy New Year'
media_order: OpSim0.02.png
published: true
date: '06-01-2018 00:00'
publish_date: '06-01-2018 00:00'
metadata:
    author: admin
taxonomy:
    category:
        - General
slug: happy-new-year
visible: true
header_image: '1'
header_image_file: OpSim0.02.png
summary:
    enabled: '1'
    format: short
    size: 128
author: admin
---

**Happy new year to all!**
Let’s start with the good news first. OpSim 0.02 is expected to see first light in 2018! Behind the screens a lot of things happened, though less than desired. I’m struggling with my daytime job, personal life and other interests as everyone does. Developing OpSim is only a small aspect of my occupations. However, developing OpSim and creating something from the ground up is my long term goal. Anyone interested in this journey and willing to participate in any form is greatly appreciated and welcomed.

The most apparent change last year was that the OpSim repository has moved from [SourceForge](https://sourceforge.net/projects/opsim/) to [GitHub](https://github.com/daar/opsim). There are a couple of reasons behind this but mainly it has to do with better tools and tighter integration. Invisible to everyone, but the [opsim.cc](http://opsim.cc) website is now self hosted as well. This means that SF is dropped completely, also for the documentation. This resides on it’s own subdomain see [here](http://opsim.cc/documentation/).

So what about the code? Well, not as much as I was hoping for I’m afraid. At least not visible in the repository. In total only 19 commits were made over 2017. These commits were mainly work on the documentation. Fortunately the ANT library is now functioning on Windows and if I remember correctly on Linux as well. macOS will be supported later. The ANT library is a minimal context handling library (like Glut or GLFW) specifically designed from OpSim. This allows an optimal integration and easy adjustment of the API as needed. More work has been done on other projects like PMake and the ISE that impact OpSim but do not show up in the commits.

PMake, the designated build system for OpSim is in a rewrite. Some bad design decisions were made which require the rewrite. In total about 30 commits were made in 2017. PMake is a fundamental part of an efficient OpSim development and is a prerequisite before 0.02 can be released.

On the ISE project also quite some work has been done. Unfortunately since my last [post](http://opsim.cc/first-light-for-the-new-user-interface/) on this topic, my laptop was struck with a ransomware virus. That means that all work was lost and I had to start from scratch again. However this gave me opportunity to redo the design and make some improvements along the way. Currently the initialization code is ported from the C sources and I am working on the display. The plan is to integrate it with the ANT library and then commit a WIP version in the GIT master branch.

**Plans for 2018**  
Fortunately I have enough plans! 🙂 But releasing OpSim 0.02, is definitely high up the list. I really hope to get some other people on-board that can help me with the development, although I do realise that having a version 0.02 that lays the foundation for the coming years is required. If you like to stay informed on the progress, please check out the [projects](https://github.com/daar/opsim/projects/1) page on GitHub. After the release the fun part will come, planning for 0.03!!! I can’t wait.

For everyone interested in the project, please keep following this project and if you are up to the challenge, let [me](mailto:darius@opsim.cc) know. For all others, I whish you a great 2018!