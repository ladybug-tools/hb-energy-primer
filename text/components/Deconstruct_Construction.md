## Deconstruct Construction

![](../../images/components/Deconstruct_Construction.png)

![](../../images/icons/Deconstruct_Construction.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Deconstruct%20Construction.py)


Deconstruct an opaque or window construction into its constituient materials. 



#### Inputs
* ##### constr [Required]
An opaque or window construction to be deconstructed. This can also be text for an opaque or window construction to be looked up in the construction library. 

#### Outputs
* ##### materials
List of material objects that make up the construction (ordered from outside to inside). 
* ##### layers
List of material identifiers that make up the construction (ordered from outside to inside). 
* ##### r_val_si
R-value of the construction in m2-K/W. Note that R-values do NOT include the resistance of air films on either side of the construction. 
* ##### r_val_ip
R-value of the construction in h-ft2-F/Btu. Note that R-values do NOT include the resistance of air films on either side of the construction. 
* ##### u_fac_si
U-factor of the construction in W/m2-K.  Note that U-factors include the resistance of air films on either side of the construction. 
* ##### u_fac_ip
U-factor of the construction in Btu/h-ft2-F.  Note that U-factors include the resistance of air films on either side of the construction. 
* ##### shgc
The estimated solar heat gain coefficient (SHGC) of the construction. This value is produced by finding the solution to the relationship between U-value, Solar Transmittance, and SHGC as defined for the simple glazing system material in EnergyPlus. More information can be found at https://bigladdersoftware.com/epx/docs/9-5/engineering-reference/ on this partticular sub-page of the engineering reference: window-calculation-module.html#step-4.-determine-layer-solar-transmittance 
* ##### t_sol
The unshaded shortwave solar transmittance of the construction at normal incidence. Note that 'unshaded' in this case means that all blind + shade materials in the construction are ignored. 
* ##### t_vis
The unshaded visible transmittance of the window at normal incidence. Note that 'unshaded' in this case means that all blind + shade materials in the construction are ignored. 