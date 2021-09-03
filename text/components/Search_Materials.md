## Search Materials

![](../../images/components/Search_Materials.png)

![](../../images/icons/Search_Materials.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Search%20Materials.py)


Search for available Materials within the honeybee energy standards library. 



#### Inputs
* ##### keywords 
Optional keywords to be used to narrow down the output list of materials. If nothing is input here, all available materials will be output. 
* ##### join_words 
If False or None, this component will automatically split any strings of multiple keywords (spearated by spaces) into separate keywords for searching. This results in a greater liklihood of finding an item in the search but it may not be appropropriate for all cases. You may want to set it to True when you are searching for a specific phrase that includes spaces. Default: False. 

#### Outputs
* ##### opaque_mats
A list of opaque materials within the honeybee energy standards library (filtered by keywords_ if they are input). 
* ##### window_mats
A list of window materials within the honeybee energy standards library (filtered by keywords_ if they are input). 