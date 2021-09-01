# Read Custom Result

![](../../.gitbook/assets/Read_Custom_Result.png)

![](../../.gitbook/assets/Read_Custom_Result%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Read%20Custom%20Result.py)

Parse any time series data from an energy simulation SQL result file.

## Inputs

* **sql \[Required\]**

  The file path of the SQL result file that has been generated from an energy simulation. 

* **output\_names \[Required\]**

  A list of EnergyPlus output names as strings \(eg. 'Surface Window System Solar Transmittance'. These data corresponding to these outputs will be returned from this component. 

## Outputs

* **results**

  DataCollections for the output\_names. 

