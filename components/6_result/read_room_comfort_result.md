# Read Room Comfort Result

![](../../.gitbook/assets/Read_Room_Comfort_Result.png)

![](../../.gitbook/assets/Read_Room_Comfort_Result%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Read%20Room%20Comfort%20Result.py)

Parse all of the common Room-level comfort-related results from an SQL result file that has been generated from an energy simulation.

## Inputs

* **sql \[Required\]**

  The file path of the SQL result file that has been generated from an energy simulation. 

## Outputs

* **oper\_temp**

  DataCollections for the mean operative temperature of each room \(C\). 

* **air\_temp**

  DataCollections for the mean air temperature of each room \(C\). 

* **rad\_temp**

  DataCollections for the mean radiant temperature of each room \(C\). 

* **rel\_humidity**

  DataCollections for the relative humidity of each room \(%\). 

