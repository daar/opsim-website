---
title: 'Development of a simulation engine'
published: false
date: '08-04-2016 00:00'
publish_date: '08-04-2016 00:00'
metadata:
    author: admin
taxonomy:
    category:
        - Planning
visible: true
content:
    items: '@self.children'
    limit: '5'
    order:
        by: date
        dir: desc
    pagination: '1'
    url_taxonomy_filters: '1'
summary:
    enabled: '1'
    format: short
    size: 128
author: admin
---

After careful planning, designing, adjustments and refactoring a simulation engine has been designed for OpSim. The simulation engine is based on an expandable data structure. For now we have implemented simplex and genetic algorithm (GA) solvers.

**Data structure**  
 The internal data structure is built up around 4 different structures as shown in the figure below.

<image>

The top level structure is the *SimulationCase* record. This data structure holds all submodels called blocks in the *ModelBlock* structure. In future OpSim will possibly allow also to load and link multiple simulation cases, but this is out of scope for the moment.

The *ModelBlock* data structure holds a list of *ModelEquations*. These equations are parsed into a tree that can quickly be evaluated to calculate the equation residuals. The residuals are input for the GA and simplex solvers.

The basic data structure is the *ModelVariable*. This data structure holds a reference to each model variable including some additional variables. One of these variables is *specification*. The specification determines if a variable is seen as constant (Fixed) or will be estimated by the solver in the case it is Free.

**Solver**  
 Currently there are two different solvers implemented. The first solver is the well known simplex solver. This solver works on the principle of …

Next a GA solver has been implemented.