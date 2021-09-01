# IdealAir

![](../../.gitbook/assets/IdealAir.png)

![](../../.gitbook/assets/IdealAir%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20IdealAir.py)

Apply a customized IdealAirSystem to Honeybee Rooms.

## Inputs

* **rooms \[Required\]**

  Honeybee Rooms to which the input ideal air properties will be assigned. This can also be a Honeybee Model for which all conditioned Rooms will be assigned the ideal air system. 

* **economizer**

  Text to indicate the type of air-side economizer used on the ideal air system. Economizers will mix in a greater amount of outdoor air to cool the zone \(rather than running the cooling system\) when the zone needs cooling and the outdoor air is cooler than the zone. Choose from the options below. Default: DifferentialDryBulb.

  * NoEconomizer
  * DifferentialDryBulb
  * DifferentialEnthalpy

* **dcv**

  Boolean to note whether demand controlled ventilation should be used on the system, which will vary the amount of ventilation air according to the occupancy schedule of the zone. Default: False. 

* **sensible\_hr**

  A number between 0 and 1 for the effectiveness of sensible heat recovery within the system. Default: 0. 

* **latent\_hr**

  A number between 0 and 1 for the effectiveness of latent heat recovery within the system. Default: 0. 

* **heat\_temp**

  A number for the maximum heating supply air temperature \[C\]. Default: 50, which is typical for many air-based HVAC systems. 

* **cool\_temp**

  A number for the minimum cooling supply air temperature \[C\]. Default: 13, which is typical for many air-based HVAC systems. 

* **heat\_limit**

  A number for the maximum heating capacity in Watts. This can also be the text 'autosize' to indicate that the capacity should be determined during the EnergyPlus sizing calculation. This can also be the text 'NoLimit' to indicate no upper limit to the heating capacity. Default: 'autosize'. 

* **cool\_limit**

  A number for the maximum cooling capacity in Watts. This can also be the text 'autosize' to indicate that the capacity should be determined during the EnergyPlus sizing calculation. This can also be the text 'NoLimit' to indicate no upper limit to the cooling capacity. Default: 'autosize'. 

## Outputs

* **report**

  The execution information, as output and error streams 

* **rooms**

  The input Rooms with their Ideal Air Systems edited. 

