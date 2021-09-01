# Deconstruct Hot Water

![](../../.gitbook/assets/Deconstruct_Hot_Water.png)

![](../../.gitbook/assets/Deconstruct_Hot_Water%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Deconstruct%20Hot%20Water.py)

Deconstruct a ServiceHotWater object into its constituient properties.

## Inputs

* **hot\_water \[Required\]**

  A ServiceHotWater object to be deconstructed. 

## Outputs

* **name**

  An Equipment object that can be used to create a ProgramType or be assigned directly to a Room. 

* **flow\_per\_area**

  A numerical value for the total volume flow rate of water per unit area of floor \(L/h-m2\). 

* **schedule**

  A fractional schedule for the use of hot water over the course of the year. The fractional values will get multiplied by the \_flow\_per\_area to yield a complete water usage profile. 

* **target\_temp**

  The target temperature of the water out of the tap in Celsius. This the temperature after the hot water has been mixed with cold water from the water mains. 

* **sensible\_fract**

  A number between 0 and 1 for the fraction of the total hot water load given off as sensible heat in the zone. 

* **latent\_fract**

  A number between 0 and 1 for the fraction of the total hot water load that is latent \(as opposed to sensible\). 

