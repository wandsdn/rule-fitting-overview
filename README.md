This repository contains an overview of the code and evaluation artifacts I created during my PhD. The main focus of my thesis was to enable a network operator to easily deploy existing SDN applications to incompatible hardware devices by algorithmically fitting existing application's ruleset to an incompatible constrained fixed-function pipeline. My thesis is being marked; a link will follow.

### Rule-fitting

#### [ofsolver](https://github.com/wandsdn/ofsolver) 
A rule-fitting solver to transform an OpenFlow 1.3 ruleset to a new constrained fixed-function pipeline. The solver is primarily written in Python and depends on the ofequivalence and ttp-tools libraries described below. This code includes an implementation of the rule-fitting technique which I describe and evaluate in my thesis, which uses SAT constraints to narrow the search to find valid solutions.

#### [minisat-zmq](https://github.com/wandsdn/minisat-zmq)
A zmq interface to the [Minisat2](http://minisat.se/) SAT solver. Ofsolver uses minisat-zmq to interface with the Minisat solver.

#### [ofsolver-evaluation](https://github.com/wandsdn/ofsolver-evaluation)
The rulesets and pipelines I used for evaluation of ofsolver and the raw results I collected.

### Ruleset Equivalence

#### [ofequivalence](https://github.com/wandsdn/ofequivalence)
A tool to convert an OpenFlow 1.3 ruleset's forwarding behaviour to a canonical MTBDD which is trivially comparable with another.  The code is primarily written in Python. We published this work to SOSR19: [Identifying Equivalent SDN Forwarding Behaviour](https://doi.org/10.1145/3314148.3314347), _Richard Sanger, Matthew Luckie, Richard Nelson_.

### Table Type Patterns

#### [ttp-tools](https://github.com/wandsdn/ttp-tools)
A library and set of tools for working with [Table Type Patterns](https://www.opennetworking.org/wp-content/uploads/2013/04/OpenFlow%20Table%20Type%20Patterns%20v1.0.pdf) (TTPs). This library verifies the validity of a TTP and parses it into an internal representation. The library includes tools to view and verify TTPs and code to place OpenFlow rules into the pipeline described by a TTP.

#### [flask-ttp-validator](https://github.com/wandsdn/flask-ttp-validator)
A Flask web application for validating a Table Type Pattern. An online version is avaliable [here](https://wand.net.nz/ttp-validator/).


### OpenFlow switch packet-in and out (slow-path) performance
This research was not included in my thesis but was published during my PhD. We published this work to NFV-SDN 2018: [Characterising the Limits of the OpenFlow Slow-Path](https://doi.org/10.1109/NFV-SDN.2018.8725766), _Richard Sanger, Brad Cowie, Matthew Luckie, Richard Nelson_.

#### [oflops-turbo](https://github.com/wandsdn/oflops-turbo)
A modified version of oflops-turbo with support for new versions of OpenFlow (including 1.3) and with encrypted control-channel support.

#### [evaluation artifacts](https://wand.net.nz/files/slow-path/)
The evaluation artifacts and scripts from our paper.
