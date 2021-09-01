# Interior Construction Subset

![](../../.gitbook/assets/Interior_Construction_Subset.png)

![](../../.gitbook/assets/Interior_Construction_Subset%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Interior%20Construction%20Subset.py)

Create a list of interior constructions that can be used to edit or create a ConstructionSet object.

## Inputs

* **interior\_wall**

  A construction object for interior walls \(or text for the identifier of the construction within the library\). 

* **ceiling**

  A construction object for ceilings \(or text for the identifier of the construction within the library\). 

* **interior\_floor**

  A construction object for interior floors \(or text for the identifier of the construction within the library\). 

* **interior\_window**

  A construction object for all apertures with a Surface boundary condition. This can also be text for the identifier of the construction within the library. 

* **interior\_door**

  A construction object for all opaque doors with a Surface boundary condition. This can also be text for the identifier of the construction within the library. 

* **int\_glass\_door**

  A construction object for all glass doors with a Surface boundary condition. This can also be text for the identifier of the construction within the library. 

## Outputs

* **interior\_set**

  A list of interior constructions that can be used to edit or create a ConstructionSet object. 

