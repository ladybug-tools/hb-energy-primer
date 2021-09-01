# Equipment

![](../../.gitbook/assets/Equipment.png)

![](../../.gitbook/assets/Equipment%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Equipment.py)

Create an Equipment object that can be used to specify equipment usage in a ProgramType.

## Inputs

* **name**

  Text to set the name for the Equipment and to be incorporated into a unique Equipment identifier. If None, a unique name will be generated. 

* **watts\_per\_area \[Required\]**

  A numerical value for the equipment power density in Watts per square meter of floor area. 

* **schedule \[Required\]**

  A fractional schedule for the use of equipment over the course of the year. The fractional values will get multiplied by the \_watts\_per\_area to yield a complete equipment profile. 

* **radiant\_fract**

  A number between 0 and 1 for the fraction of the total equipment load given off as long wave radiant heat. \(Default: 0\). 

* **latent\_fract**

  A number between 0 and 1 for the fraction of the total equipment load that is latent \(as opposed to sensible\). \(Default: 0\). 

* **lost\_fract**

  A number between 0 and 1 for the fraction of the total equipment load that is lost outside of the zone and the HVAC system. Typically, this is used to represent heat that is exhausted directly out of a zone \(as you would for a stove\). \(Default: 0\). 

* **gas**

  Set to "True" to have the output Equipment object be for GasEquipment \(as opposed to ElectricEquipment\). 

## Outputs

* **equip**

  An Equipment object that can be used to specify equipment usage in a ProgramType. 

