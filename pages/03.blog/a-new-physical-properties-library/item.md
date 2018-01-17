---
title: 'A new physical properties library'
media_order: physprops.png
published: true
date: '20-08-2016 00:00'
publish_date: '20-08-2016 00:00'
metadata:
    author: admin
taxonomy:
    category:
        - Coding
slug: a-new-physical-properties-library
visible: true
header_image: '1'
header_image_file: physprops.png
summary:
    enabled: '1'
    format: short
    size: 128
author: admin
---

Here’s a new addition to OpSim! In revision [390](https://sourceforge.net/p/opsim/code/390/) I have moved the physical properties (PP) library from my working branch to trunk. Together with this library the beginnings of the physical properties database has been imported into trunk. In total 57 components have been entered into the database with models for currently still only a few physical properties. With this library we are taking a large step towards a proper physical simulation environment.  
  
**Physical properties models**  
 There are currently 35 different physical property models defined in the code. These are all preliminary described in the [user documentation](http://opsim.sourceforge.net/user-docs/html/physical_properties.html). The component properties are stored in the human readable [JSON](http://www.json.org/) format. The advantage of this format is that it is very easy to read, interpret and modify physical property definitions. Even with general tools like text or JSON editors, or scripts and macro’s. One can easily export data from other databases and create a physical property definition for new components or adjust an existing component without the need of complex editors. Of course OpSim will provide a built in editor in the future, but that is of later concern.

**Properties database**  
 The PP database currently only supports two different physical properties for the defined components, namely vapour pressure and molar heat capacity for gas. This is not much yet, however implementing more properties is trivial, though a lot of work. For the properties database a number of different resources have been consulted. One of the better known resources is [NIST](http://webbook.nist.gov/chemistry/). Next to that the book *[Chemical properties handbook](http://www.amazon.com/Chemical-Properties-Handbook-Thermodynamics-Engironmental/dp/0070734011%3FSubscriptionId%3D1QHATGVD8Y4FXMDMBXG2%26tag%3Dwebofkeisai-20%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D0070734011)* was a very helpful resource.  
 I would really welcome all help in adding more components and properties to our database, provided the information is allowed to be used of course and that a clear reference is supplied. I’m looking forward in getting help to create and update the OpSim model files from other resources and databases. So if you would like to help out here, please contact me either via the [forum](https://groups.google.com/forum/#!forum/opsim) or one of the [mailing lists](https://sourceforge.net/p/opsim/mailman/).

**Future considerations**  
 The PP library can and will be improved in many aspects. One of these areas is caching of PP models instead of loading them all at start-up. Another improvement will be the handling of units and unit conversions. The current code uses a brute force conversion of the input and output units of the models. Hardly efficient, but it gets the work done. It needs to be evaluated if this is the best design when large simulations will be at work. Lastly, of course the always occurring memory leaks need to be addressed.

-Darius-