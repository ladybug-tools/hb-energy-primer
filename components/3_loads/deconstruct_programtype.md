# Deconstruct ProgramType

![](../../.gitbook/assets/Deconstruct_ProgramType.png)

![](../../.gitbook/assets/Deconstruct_ProgramType%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Deconstruct%20ProgramType.py)

Deconstruct a ProgramType object into its component load objects.

## Inputs

* **program \[Required\]**

  A ProgramType object or text for the identifier of a ProgramType to be looked up in the program type library. 

## Outputs

* **people**

  A People object that describes the occupancy of the program. If None, no people are assumed to occupy the program. 

* **lighting**

  A Lighting object that describes the lighting usage of the program. If None, no lights are assumed to be installed. 

* **electric\_equip**

  An ElectricEquipment object to describe the usage of electric equipment within the program. If None, no electric equipment is assumed to be installed. 

* **gas\_equip**

  A GasEquipment object to describe the usage of gas equipment within the program. If None, no gas equipment is assumed to be installed. 

* **hot\_water**

  A ServiceHotWater object to describe the usage of hot water within the program. If None, no hot water is be assumed for the program. 

* **infiltration**

  An Infiltration object to describe the outdoor air leakage of the program. If None, no infiltration is be assumed for the program. 

* **ventilation**

  A Ventilation object to describe the minimum outdoor air requirement of the program. If None, no ventilation requirement is be assumed for the program. 

* **setpoint**

  A Setpoint object to describe the temperature and humidity setpoints of the program.  If None, the ProgramType cannot be assigned to a Room that is conditioned. 

