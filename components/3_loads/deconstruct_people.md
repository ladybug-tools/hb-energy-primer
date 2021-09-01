# Deconstruct People

![](../../.gitbook/assets/Deconstruct_People.png)

![](../../.gitbook/assets/Deconstruct_People%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Deconstruct%20People.py)

Deconstruct a People object into its constituient properties.

## Inputs

* **people \[Required\]**

  A People object to deconstruct. 

## Outputs

* **name**

  Text string for the people object display name. 

* **ppl\_per\_area**

  A numerical value for the number of people per square meter of floor area. 

* **occupancy\_sch**

  A fractional schedule for the occupancy over the course of the year. The fractional values in this schedule get multiplied by the \_people\_per\_area to yield a complete occupancy profile. 

* **activity\_sch**

  A schedule for the activity of the occupants over the course of the year. The type limt of this schedule are "Power" and the values of the schedule equal to the number of Watts given off by an individual person in the room. 

