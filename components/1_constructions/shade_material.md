# Shade Material

![](../../.gitbook/assets/Shade_Material.png)

![](../../.gitbook/assets/Shade_Material%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Shade%20Material.py)

Create a material for a shade layer in a window construction \(like a roller shade\). This material can be plugged into the "HB Window Construction" component.

Reflectance and emissivity properties are assumed to be the same on both sides of the shade. Shades are considered to be perfect diffusers.

## Inputs

* **name**

  Text to set the name for the material and to be incorporated into a unique material identifier. 

* **thickness \[Required\]**

  Number for the thickness of the shade layer in meters. 

* **transmittance**

  Number between 0 and 1 for the transmittance of both solar radiation and visible light through the shade. \(Default: 0.4, which is typical of a white diffusing shade\). 

* **reflectance**

  Number between 0 and 1 for the reflectance of both solar radiation and visible light off of the shade. \(Default: 0.5, which is typical of a white diffusing shade\). 

* **t\_infrared**

  Long-wave hemisperical transmittance of the shade. \(Default: 0\). 

* **emissivity**

  Number between 0 and 1 for the infrared hemispherical emissivity of the shade. \(Default: 0.9, which is typical of most diffusing shade materials\). 

* **conductivity**

  Number for the thermal conductivity of the shade in W/m-K. \(Default: 0.05, typical of cotton shades\). 

* **dist\_to\_glass**

  A number between 0.001 and 1.0 for the distance between the shade and neighboring glass layers \[m\]. \(Default: 0.05 \(50 mm\)\). 

* **open\_mult**

  Factor between 0 and 1 that is multiplied by the area at the top, bottom and sides of the shade for air flow calculations. \(Default: 0.5\). 

* **permeability**

  The fraction of the shade surface that is open to air flow. Must be between 0 and 0.8. \(Default: 0 for no permeability\). 

## Outputs

* **mat**

  A material for a shade layer in a window construction \(like a roller shade\) that can be assigned to a Honeybee Window construction. 

