# Read Thermal Matrix

![](../../.gitbook/assets/Read_Thermal_Matrix.png)

![](../../.gitbook/assets/Read_Thermal_Matrix%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Read%20Thermal%20Matrix.py)

Read the detailed results of a thermal mapping analysis from a folder of CSV files output by a thermal mapping component.

Detailed results include temperature amd thermal condition results. It also includes metrics that give a sense of how hot or cold condition are like pmv, utci category, or adaptive comfort degrees from neutral temperature.

## Inputs

* **comf\_result \[Required\]**

  Path to a folder containing CSV files output by a thermal mapping component. 

* **load \[Required\]**

  Set to True to load the data from the CSV files into Grasshopper. 

## Outputs

* **comf\_mtx**

  A Matrix object that can be connected to the "HB Visualize Thermal Map" component in order to spatially visualize results. This Matrix object can also be connected to the "LB Deconstruct Matrix" component to obtain detailed point-by-point and hour-by-hour values. 

  When deconstructed, each sub-list of the matrix \(aka. branch of the Data Tree\) represents one of the sensor grids used for analysis. The length of each sub-list matches the number of points in the grid. Each value in the sub-list is an hourly data collection containing hour-by-hour results for each point. 

