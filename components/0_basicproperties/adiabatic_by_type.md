# Adiabatic by Type

![](../../.gitbook/assets/Adiabatic_by_Type.png)

![](../../.gitbook/assets/Adiabatic_by_Type%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Adiabatic%20by%20Type.py)

Make boundary conditions of Rooms or Faces adiabatic by face type.

## Inputs

* **hb\_objs \[Required\]**

  Honeybee Faces or Rooms to which adiabatic boundary conditions will be assigned. 

* **exterior\_walls**

  If True, all exterior walls of the input Rooms or Faces will be set to adiabatic. This can also be a list of boolean values and different adiabatic values will be assigned based on the cardinal direction, starting with north and moving clockwise. 

* **roofs**

  If True, all exterior roofs of the input Rooms or Faces will be set to adiabatic. 

* **exposed\_floors**

  If True, all exposed floors of the input Rooms or Faces will be set to adiabatic. 

* **interior\_walls**

  If True, all interior walls of the input Rooms or Faces will be set to adiabatic. 

* **interior\_floors**

  If True, all interior floors and ceilings of the input Rooms or Faces will be set to adiabatic. 

## Outputs

* **hb\_objs**

  The input honeybee objects with their boundary conditions edited. 

