## Apply Load Values

![](../../images/components/Apply_Load_Values.png)

![](../../images/icons/Apply_Load_Values.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Apply%20Load%20Values.py)


Apply load values to a Room or ProgramType. 

This component will not edit any of the schedule objects associated with each load value. If no schedule currently exists to describe how the load varies over the simulation, the "Always On" schedule will be used as a default. 



#### Inputs
* ##### room_or_program [Required]
Honeybee Rooms or ProgramType objects to which the input load objects should be assigned. This can also be the identifier of a ProgramType to be looked up in the program type library. 
* ##### people_per_floor 
A numerical value for the number of people per square meter of floor area. 
* ##### lighting_per_floor 
A numerical value for the lighting power density in Watts per square meter of floor area. 
* ##### electric_per_floor 
A numerical value for the electric equipment power density in Watts per square meter of floor area. 
* ##### gas_per_floor 
A numerical value for the gas equipment power density in Watts per square meter of floor area. 
* ##### hot_wtr_per_floor 
A numerical value for the total volume flow rate of water per unit area of floor in (L/h-m2). 
* ##### infilt_per_exterior 
A numerical value for the intensity of infiltration in m3/s per square meter of exterior surface area. Typical values for this property are as follows (note all values are at typical building pressures of ~4 Pa): 

    * 0.0001 (m3/s per m2 facade) - Tight building

    * 0.0003 (m3/s per m2 facade) - Average building

    * 0.0006 (m3/s per m2 facade) - Leaky building
* ##### vent_per_floor 
A numerical value for the intensity of ventilation in m3/s per square meter of floor area. 
* ##### vent_per_person 
A numerical value for the intensity of ventilation in m3/s per person. Note that setting this value here does not mean that ventilation is varied based on real-time occupancy but rather that the design level of ventilation is determined using this value and the People object of the zone. To vary ventilation in real time, the ventilation schedule should be used. Most ventilation standards support that a value of 0.01 m3/s (10 L/s or ~20 cfm) per person is sufficient to remove odors. Accordingly, setting this value to 0.01 and using 0 for the following ventilation terms will often be suitable for many applications. 

#### Outputs
* ##### report
Reports, errors, warnings, etc. 
* ##### mod_obj
The input Rooms or ProgramTypes with their load values modified. 