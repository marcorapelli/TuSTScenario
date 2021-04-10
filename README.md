# Turin SUMO Traffic (TuST) Scenario

Contacts: Marco RAPELLI [rapelli.m@libero.it], Claudio CASETTI [claudio.casetti@polito.it] and Giandomenico GAGLIARDI [giandomenico.gagliardi@5T.torino.it]

This project is licensed under the terms of the GPLv3 license.

Please refer to the [SUMO wiki](http://sumo.dlr.de/wiki/Simulation_of_Urban_MObility_-_Wiki) for further information on the simulator itself.

**Due to the size of the considered scenario, input and output files may exceed the GitHub maximum file size limit of 100 MB.**
**For this reason it is required to use [Git LFS](https://git-lfs.github.com) to download files.**

## Overview

The _TuST (Turin SUMO Traffic)_ simulation scenario describes the traffic within the city of Turin, Italy for a whole day. The original demand data stems from real traffic data of 5T, a public agency managing all the traffic mobility data in the Italian region of Piemonte.

From the original OSM file, an accurate road graph was created using real average velocities from Google APIs and real traffic light phases from 5T data.

To validate the model, traffic flows were compared to real flows measured from 5T street sensors, creating in this way a very realistic large-scale simulator.

#### Case Study Map

![Case Study Map](Map_Km.png)

#### Important Note

_TuST Scenario has been developed with_ [SUMO 1.1.0](https://github.com/eclipse/sumo/tree/v1_1_0) _and it has been successfully tested also with_ [SUMO 1.2.0](https://github.com/eclipse/sumo/tree/v1_2_0) _and_ [SUMO 1.3.1](https://github.com/eclipse/sumo/tree/v1_3_1). _Although it is possible to use it with more recent versions of SUMO, results may differ._
_Recommended SUMO version is_ [SUMO 1.2.0](https://github.com/eclipse/sumo/tree/v1_2_0).

## How to cite it: [BibTeX](cite.bib)

Best paper award of DS-RT 2019 to M. Rapelli, C. Casetti, G. Gagliardi,
*"TuST: from Raw Data to Vehicular Traffic Simulation in Turin"*
2019 IEEE/ACM 23rd International Symposium on Distributed Simulation and Real Time Applications (DS-RT)
October, 2019, Cosenza, Italy.

## How To

The TuST scenario can be launched directly with its configuration file.
* `$SUMO_HOME/bin/sumo -c TuST.sumocfg` from the _Scenario_ folder.

In order to rebuild the routes it is possible to launch the route configuration file.
* `$SUMO_HOME/bin/marouter -c RoutingConfig.xml` from the _Scenario_ folder.

## Statistics

The TuST scenario generates a stable simulation, as highlighted by the following plot, where the number of waiting vehicles is used as a congestion metric.
It is possible to see how congestion is solved after the afternoon traffic peak.

![Stability Study](StabilityStudyGraph.png)

#### TuST in numbers

Description | Value 
--- | :---: 
Area | 602.61 Km<sup>2</sup>
Traffic Assignment Zones | 257
Nodes | 32,936
Edges | 66,296
Traffic Lights | 856
Roundabouts | 501
Total edge length | 6,570.28 Km
Total lane length | 7,723.40 Km
Final departed vehicles | 2,202,814
Final waiting vehicles | 0
Final running vehicles | 5142
Final arrived vehicles | 2,197,672
Total collisions | 0
Total teleports | 334
Total halting | 19
