## Type Limit

![](../../images/components/Type_Limit.png)

![](../../images/icons/Type_Limit.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Type%20Limit.py)


Create a custom ScheduleTypeLimit object that can be assigned to any schedule object. 

Schedule types exist for the sole purpose of validating schedule values against upper/lower limits and assigning a data type and units to the schedule values. As such, they are not necessary to run energy simulations but their use is generally considered good practice. 



#### Inputs
* ##### name [Required]
Text to set the name for the ScheduleTypeLimit. This should be unique to avoif conflcit with other schedule types. 
* ##### low_limit 
An optional number for the lower limit for values in the schedule. If None, there will be no lower limit. 
* ##### up_limit 
An optional number for the upper limit for values in the schedule. If None, there will be no upper limit. 
* ##### discrete 
Boolean to not whether the values of the schedule are continuous or discrete. The latter means that only integers are accepted as schedule values. Default: False for 'Continuous'. 
* ##### unit_type 
Text for an EnergyPlus unit type, which will be used to assign units to the values in the schedule.  Note that this field is not used in the actual calculations of EnergyPlus. Default: 'Dimensionless'. Choose from the following: 

    * Dimensionless

    * Temperature

    * DeltaTemperature

    * PrecipitationRate

    * Angle

    * ConvectionCoefficient

    * ActivityLevel

    * Velocity

    * Capacity

    * Power

    * Availability

    * Percent

    * Control

    * Mode

#### Outputs
* ##### report
Reports, errors, warnings, etc. 
* ##### type_limit
A ScheduleTypeLimit object that can be assigned to any schedule object. 