# Normalize by Floor Area

![](../../.gitbook/assets/Normalize_by_Floor_Area.png)

![](../../.gitbook/assets/Normalize_by_Floor_Area%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Normalize%20by%20Floor%20Area.py)

Normalize Zone-level data collections from an energy simulation by the by the floor area of the corresponding honeybee Rooms.

## Inputs

* **data \[Required\]**

  A list of HourlyContinuousCollections of the same data type, which will be normalized by room floor area. Data collections can be of any class \(eg. MonthlyCollection, DailyCollection\) but they should originate from an energy simulation sql \(with header metadata that has 'Zone' or 'System' keys\). These keys will be used to match the data in the collections to the input rooms. 

* **model \[Required\]**

  An array of honeybee Rooms or a honeybee Model, which will be matched to the data collections. The length of these Rooms does not have to match the data collections and this object will only output collections for rooms that are found to be matching. 

## Outputs

* **total\_data**

  The total results normalized by the floor area of all connected rooms. This accounts for the fact that some rooms have more floor area \(or have a multiplier\) and therefore get a greater weighting. 

* **room\_data**

  The results normalized by the floor area of each individual room. 

