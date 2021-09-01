# End Use Intensity

![](../../.gitbook/assets/End_Use_Intensity.png)

![](../../.gitbook/assets/End_Use_Intensity%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20End%20Use%20Intensity.py)

Get information about end use intensity from an EnergyPlus SQL file.

## Inputs

* **sql \[Required\]**

  The file path of the SQL result file that has been generated from an energy simulation. This can also be a list of EnergyPlus files in which case, EUI will be computed across all files. 

* **ip**

  Boolean to note whether the EUI should be in SI \(kWh/m2\) or IP \(kBtu/ft2\) units. \(Default: False\). 

## Outputs

* **eui**

  The total end use intensity result from the simulation. Specifically, this is the sum of all electricity, fuel, district heating/cooling, etc. divided by the gross floor area \(including both conditioned and unconditioned spaces\). The value will be in kWh/m2 if ip\_ is False or None and kBtu/ft2 if True. 

* **eui\_end\_use**

  The end use intensity result from the simulation, broken down by each end use. These values coorespond to the end_uses output below. Values will be in kWh/m2 if ip_ is False or None and kBtu/ft2 if True. 

* **end\_uses**

  A list of text for each of the end uses in the simulation \(Heating, Cooling, etc.\). Thes outputs coorespond to the eui\_end\_use output above. 

* **gross\_floor**

  The total gross floor area of the energy model. This can be used to compute the total energy use from the intensity values above or it can be used to help with other result post-processing. The value will be in m2 if ip\_ is False or None and ft2 if True. 

