## Window Gap Material

![](../../images/components/Window_Gap_Material.png)

![](../../images/icons/Window_Gap_Material.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Window%20Gap%20Material.py)


Create a window gas gap material that corresponds to a layer in a window construction. This material can be plugged into the "HB Window Construction" component. 



#### Inputs
* ##### name 
Text to set the name for the material and to be incorporated into a unique material identifier. 
* ##### thickness 
Number for the thickness of the air gap layer in meters. (Default: 0.0125 m). 
* ##### gas_types 
A list of text describing the types of gas in the gap. Text must be one of the following: 'Air', 'Argon', 'Krypton', 'Xenon'. 
* ##### gas_ratios 
A list of text describing the volumetric fractions of gas types in the mixture.  This list must align with the gas_types input list. Default: Equal amout of gases for each type. 

#### Outputs
* ##### mat
A window gas gap material that describes a layer in a window construction and can be assigned to a Honeybee Window construction. 