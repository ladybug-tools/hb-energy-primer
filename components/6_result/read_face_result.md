# Read Face Result

![](../../.gitbook/assets/Read_Face_Result.png)

![](../../.gitbook/assets/Read_Face_Result%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Read%20Face%20Result.py)

Parse all of the common Room-level comfort-related results from an SQL result file that has been generated from an energy simulation.

## Inputs

* **sql \[Required\]**

  The file path of the SQL result file that has been generated from an energy simulation. 

## Outputs

* **face\_indoor\_temp**

  DataCollections for the indoor surface temperature of each surface \(C\). 

* **face\_outdoor\_temp**

  DataCollections for the outdoor surface temperature of each surface \(C\). 

* **face\_energy\_flow**

  DataCollections for the heat loss \(negative\) or heat gain \(positive\) through each building surfaces \(kWh\). 

