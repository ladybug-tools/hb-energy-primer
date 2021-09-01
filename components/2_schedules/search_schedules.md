# Search Schedules

![](../../.gitbook/assets/Search_Schedules.png)

![](../../.gitbook/assets/Search_Schedules%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Search%20Schedules.py)

Search for available Schedules within the honeybee energy standards library.

## Inputs

* **keywords**

  Optional keywords to be used to narrow down the output list of scheduless. If nothing is input here, all available schedules will be output. 

* **join\_words**

  If False or None, this component will automatically split any strings of multiple keywords \(spearated by spaces\) into separate keywords for searching. This results in a greater liklihood of finding an item in the search but it may not be appropropriate for all cases. You may want to set it to True when you are searching for a specific phrase that includes spaces. Default: False. 

## Outputs

* **schedules**

  A list of Schedules within the honeybee energy standards library \(filtered by keywords\_ if they are input\). 

* **type\_limits**

  A list of all ScheduleTypeLimits within the honeybee energy standards library. 

