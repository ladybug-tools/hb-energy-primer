# Ventilation

![](../../.gitbook/assets/Ventilation.png)

![](../../.gitbook/assets/Ventilation%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Ventilation.py)

Create a Ventilation object that can be used to create a ProgramType or be assigned directly to a Room.

Note the the 4 ventilation types \(_flow\_per\_person_, _flow\_per\_area_, _flow\_per\_zone_, _ach_\) are ultimately summed together to yeild the ventilation design flow rate used in the simulation.

## Inputs

* **name**

  Text to set the name for the Ventilation and to be incorporated into a unique Ventilation identifier. If None, a unique name will be generated. 

* **flow\_per\_person**

  A numerical value for the intensity of ventilation in m3/s per person. Note that setting this value here does not mean that ventilation is varied based on real-time occupancy but rather that the design level of ventilation is determined using this value and the People object of the zone. To vary ventilation in real time, the ventilation schedule should be used. Most ventilation standards support that a value of 0.01 m3/s \(10 L/s or ~20 cfm\) per person is sufficient to remove odors. Accordingly, setting this value to 0.01 and using 0 for the following ventilation terms will often be suitable for many applications. Default: 0. 

* **flow\_per\_area**

  A numerical value for the intensity of ventilation in m3/s per square meter of floor area. Default: 0. 

* **flow\_per\_zone**

  A numerical value for the design level of ventilation in m3/s for the entire zone. Default: 0. 

* **ach**

  A numberical value for the design level of ventilation in air changes per hour \(ACH\) for the entire zone. This is particularly helpful for hospitals, where ventilation standards are often given in ACH. Default: 0. 

* **schedule**

  An optional fractional schedule for the ventilation over the course of the year. The fractional values will get multiplied by the total design flow rate \(determined from the fields above and the calculation\_method\) to yield a complete ventilation profile. Setting this schedule to be the occupancy schedule of the zone will mimic demand controlled ventilation. If None, the design level of ventilation will be used throughout all timesteps of the simulation. Default: None. 

## Outputs

* **vent**

  An Ventilation object that can be used to create a ProgramType or be assigned directly to a Room. 

