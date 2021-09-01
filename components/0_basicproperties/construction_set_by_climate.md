# Construction Set by Climate

![](../../.gitbook/assets/Construction_Set_by_Climate.png)

![](../../.gitbook/assets/Construction_Set_by_Climate%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Construction%20Set%20by%20Climate.py)

Get a ConstructionSet from the standards library using a climate zone, building vintage and construction type.

## Inputs

* **climate\_zone \[Required\]**

  An integer between 1 and 8 for the ASHRAE climate zone in which the building is located. ASHRAE climate zones exist for all locations on Earth and can typically be looked up online or within the .stat file that downloads next to the .epw file. The climate zone is used to determine the amount of code-recommended insulation and solar heat gain protection for the construction set. The Honeybee "Climate Zones" component lists all of the climate zones supported by the library. 

* **vintage**

  Text for the building vintage to search \(eg. "2013", "pre\_1980", etc.\). The Honeybee "Building Vintages" component lists all of the vintages available in the library. Default: "2013" \(for ASHRAE 90.1 2013\). Note that vintages are often called "templates" within the OpenStudio standards gem and so this property effective maps to the standards gem "template". 

* **constr\_type**

  Text for the construction type of the set. \(eg. "SteelFramed", "WoodFramed", "Mass", "Metal Building"\). The Honeybee "Construction Types" component lists all of the construction types available in the library. 

## Outputs

* **constr\_set**

  A ConstructionSet identifier that can be applied to Honeybee Rooms. 

