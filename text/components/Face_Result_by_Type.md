## Face Result by Type

![](../../images/components/Face_Result_by_Type.png)

![](../../images/icons/Face_Result_by_Type.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Face%20Result%20by%20Type.py)


Separate data collections of energy simulation results by object and face type. Input data must be for Faces, Apertures, Doors, or any combination of these objects. 

This component can also be used to normalize such data by area. 



#### Inputs
* ##### data [Required]
A list of data collections output from an energy simulation, which will be separated by object and face type. Data collections can be of any class (eg. MonthlyCollection, DailyCollection) but they should all have headers with metadata dictionaries with 'Surface' keys. These keys will be used to match the data in the collections to the input faces. 
* ##### hb_objs [Required]
An array of honeybee Rooms, Faces, Apertures or Doors, which will be matched with the _data. This can also be an entire Model. 
* ##### norm 
Boolean to note whether results should be normalized by the face/sub-face area if the data type of the data_colections supports it. (Default: False) 

#### Outputs
* ##### walls
Data collections with results for Walls with an Outdoors or Ground boundary condition. 
* ##### interior_walls
Data collections with results for Walls with a Surface or Adiabatic boundary condition. 
* ##### roofs
Data collections with results for RoofCeilings with an Outdoors or Ground boundary condition. 
* ##### ceilings
Data collections with results for RoofCeilings with a Surface or Adiabatic boundary condition. 
* ##### exterior_floors
Data collections with results for Floors with an Outdoors or Ground boundary condition. 
* ##### interior_floors
Data collections with results for Floors with a Surface or Adiabatic boundary condition. 
* ##### apertures
Data collections with results for Apertures with an Outdoors boundary condition. 
* ##### interior_apertures
Data collections with results for Apertures with a Surface boundary condition. 
* ##### doors
Data collections with results for Doors with an Outdoors boundary condition. 
* ##### interior_doors
Data collections with results for Doors with a Surface boundary condition. 