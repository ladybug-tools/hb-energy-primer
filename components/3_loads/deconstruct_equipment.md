# Deconstruct Equipment

![](../../.gitbook/assets/Deconstruct_Equipment.png)

![](../../.gitbook/assets/Deconstruct_Equipment%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Deconstruct%20Equipment.py)

Deconstruct an Equipment object into its constituient properties.

## Inputs

* **equip \[Required\]**

  An ElectricEquipment or a GasEquipment object to be deconstructed. 

## Outputs

* **name**

  An Equipment object that can be used to create a ProgramType or be assigned directly to a Room. 

* **watts\_per\_area**

  A numerical value for the equipment power density in Watts per square meter of floor area. 

* **schedule**

  A fractional for the use of equipment over the course of the year. The fractional values will get multiplied by the watts\_per\_area to yield a complete equipment profile. 

* **radiant\_fract**

  A number between 0 and 1 for the fraction of the total equipment load given off as long wave radiant heat. 

* **latent\_fract**

  A number between 0 and 1 for the fraction of the total equipment load that is latent \(as opposed to sensible\). 

* **lost\_fract**

  A number between 0 and 1 for the fraction of the total equipment load that is lost outside of the zone and the HVAC system. Typically, this is used to represent heat that is exhausted directly out of a zone \(as you would for a stove\). 

* **is\_gas**

  Will be True if the input Equipment object is for GasEquipment; False if it is for ElectricEquipment. 

