# Output files

## Structure

Output files stored here are divided in:
* _FullDay_ output files over the full 24h simulation.
* _MorningPeak_ output files over the morning rush hour from 8:00am to 9:00am.
* _EveningPeak_ output files over two evening rush hours from 5:00pm to 7:00pm.

## File type

In every folder three main simulation outputs are provided:
* **Summary** the simulation summary file with global metrics of the simulation.
* **DetectorsOutput** the edge-based output file from detectors placed in every edges of the map.
* **VehTraces** the completed vehicle traces file with all routes and times for every vehicle.

### Other outputs

SUMO allows the creation of many other types of output files, as referred in the dedicated [SUMO wiki page](https://sumo.dlr.de/docs/Simulation/Output.html). 

If you are interested in any of these, just add the corresponding option in the `<output>` section of the _Scenario/TuST.sumocfg_ file.
