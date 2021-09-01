# Deconstruct Schedule

![](../../.gitbook/assets/Deconstruct_Schedule.png)

![](../../.gitbook/assets/Deconstruct_Schedule%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Deconstruct%20Schedule.py)

Deconstruct a ScheduleRuleset into an array of day-long ladybug DataCollections representing each unique ScheduleDay that defines the ScheduleRuleset.

These DataCollections can be used to make visualizations of timeseries schedule values over each unique day of the schedule using a component like the "LB Line Chart".

## Inputs

* **schedule \[Required\]**

  A ScheduleRuleSet to be deconstructed into DataCollections of timeseries schedule values for each unique day. This can also be the identifier of a Schedule to be looked up in the schedule library. 

* **timestep**

  An integer for the number of steps per hour at which to make the resulting daily DataCollections. 

## Outputs

* **day\_names**

  A list of display names for each unique ScheduleDay that defines the input ScheduleRuleset. 

* **day\_data**

  A list of day-long ladybug DataCollections representing each unique ScheduleDay that defines the ScheduleRuleset. These can be used to make visualizations of timeseries schedule values over each day of the schedule using a component like the "LB Line Chart". 

* **type\_limit**

  The ScheduleTypeLimit object assigned to the ScheduleRuleset. 

