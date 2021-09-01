# Peak Loads

![](../../.gitbook/assets/Peak_Loads.png)

![](../../.gitbook/assets/Peak_Loads%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Peak%20Loads.py)

Run Honeybee Rooms through a quick energy simulation to obtain an estimate of room-level peak cooling and heating on summer and winter design days.

## Inputs

* **rooms \[Required\]**

  A list of Honeybee Rooms for which peak loads will be computed. 

* **shades**

  An optional list of Honeybee Shades that can block the sun to the input \_rooms. 

* **ddy\_file \[Required\]**

  Path to a .ddy file on your system as a text string, which contains design day conditions for the peak load analysis. This can also be the path to an .epw file, in which case design days will be determined by statitically analysing the annual data to approximate 0.4% and 99.6% design conditions. Note that .ddy files can also be created using the "DF Construct Design Day" and "DF Write DDY" components. 

  When constructing custom design days, it is recommended that the .ddy file contain only one summer and one winter design day. If mutliple summer or winter design days are found, they will be filtered according to their name in order to identify the 0.4% and 99.6% design conditions for the sensible \(dry bulb temperature\) design days. 

* **timestep**

  An integer for the number of timesteps per hour at which the energy simulation will be run and results reported. It is recommended that this be at least 6 but it can be increased to better capture the minute in which peak cooling occurs. \(Default: 6\). The following values are acceptable: \(1, 2, 3, 4, 5, 6, 10, 12, 15, 20, 30, 60\) 

* **run\_bal**

  Set to True to have the load balance computed after the simulation is run. This ensures that data collections for various terms of the load balance are output from the "balance". This can help explain why the loads are what they are but can also increase the component run time. \(Default: False\). 

* **run \[Required\]**

  Set to "True" to run the simulation to obtain annual loads. This can also be the integer 2 to run the simulation while being able to see the simulation process \(with a batch window\). 

## Outputs

* **report**

  A report of the energy simulation run. 

* **peak\_cool**

  A list of numbers that align with the input \_rooms and correspond to the peak cooling of each room on the summer design day in Watts. Note that, for multi-room simulations, the individual room peaks may not be coincident, meaning that summing these values together won't give a correct sense of the size of cetral cooling equipment serving multiple rooms. For such equipment, the max of the cooling data collection should be used. 

* **peak\_heat**

  A list of numbers that align with the input \_rooms and correspond to the peak heating of each room on the winter design day in Watts. Note that, for multi-room simulations, the individual room peaks may not be coincident, meaning that summing these values together won't give a correct sense of the size of cetral heating equipment serving multiple rooms. For such equipment, the max of the heating data collection should be used. 

* **cooling**

  A Data Collection indicating the combined cooling demand of the rooms at each simulation timestep of the summer design day. This can be plugged into the "LB Monthly Chart" component to visualize the demand or it can be deconstructed with the "LB Deconstruct Data" component for analysis. 

* **heating**

  A Data Collection indicating the combined heating demand of the rooms at each simulation timestepof the winter design day. This can be plugged into the "LB Monthly Chart" component to visualize the demand or it can be deconstructed with the "LB Deconstruct Data" component for analysis. 

* **cool\_bal**

  A list of data collections for the various terms of the sensible load balance that contribute to peak cooling on the summer design day. These can be plugged into the "LB Monthly Chart" component \(with stack _set to True\) to visualize the terms contributing to the peak. Will be None unless run\_bal_ is set to True. 

* **heat\_bal**

  A list of data collections for the various terms of the sensible load balance that contribute to peak heating on the summer design day. These can be plugged into the "LB Monthly Chart" component \(with stack _set to True\) to visualize the terms contributing to the peak. Will be None unless run\_bal_ is set to True. 

