# Deconstruct ConstructionSet Interior

![](../../.gitbook/assets/Deconstruct_ConstructionSet_Interior.png)

![](../../.gitbook/assets/Deconstruct_ConstructionSet_Interior%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Deconstruct%20ConstructionSet%20Interior.py)

Deconstruct a construction set into its constituient interior constructions.

## Inputs

* **constr\_set \[Required\]**

  A construction set to be deconstructed. This can also be text for a construction set to be looked up in the construction set library. 

## Outputs

* **interior\_wall**

  A construction object for the set's interior walls. 

* **ceiling**

  A construction object for the set's interior roofs. 

* **interior\_floor**

  A construction object for the set's interior floors. 

* **interior\_window**

  A construction object for all apertures with a Surface boundary condition. 

* **interior\_door**

  A construction object for all opaque doors with a Surface boundary condition. 

* **int\_glass\_door**

  A construction object for all glass doors with a Surface boundary condition. 

