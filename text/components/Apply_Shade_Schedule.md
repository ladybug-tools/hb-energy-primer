## Apply Shade Schedule

![](../../images/components/Apply_Shade_Schedule.png)

![](../../images/icons/Apply_Shade_Schedule.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Apply%20Shade%20Schedule.py)


Apply a transmittance schedule to Honeybee Shade objects. Alternatively, it can assign a transmittance schedule to all of the child shades of an Aperture, Door, Face, or a Room. 

This component supports the assigning of different schedules based on cardinal orientation, provided that a list of transmittance schedule are input to the _trans_sch.  



#### Inputs
* ##### hb_objs [Required]
Honeybee Shades, Apertures, Door, Faces, or Rooms to which the input _trans_sch should be assigned. For the case of a Honeybee Aperture, Door, Face or Room, the ShadeConstruction will be assigned to only the child shades directly assigned to that object. So passing in a Room will not change the schedule of shades assigned to Apertures of the Room's Faces. If this is the desired outcome, then the Room should be deconstructed into its child objects before using this component. 
* ##### trans_sch [Required]
A Honeybee ScheduleRuleset or ScheduleFixedInterval to be applied to the input _hb_objs. This can also be text for a schedule to be looked up in the shade schedule library. If an array of text or schedule objects are input here, different schedules will be assigned based on cardinal direction, starting with north and moving clockwise. 

#### Outputs
* ##### hb_objs
The input honeybee objects with their shade transmittance schedules edited. 