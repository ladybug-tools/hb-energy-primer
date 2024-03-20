## Sizing Parameter

![](../../images/components/Sizing_Parameter.png)

![](../../images/icons/Sizing_Parameter.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Sizing%20Parameter.py)


Create parameters with criteria for sizing the heating and cooling system. 



#### Inputs
* ##### ddy_file 
An optional path to a .ddy file on your system, which contains information about the design days used to size the hvac system. If None, honeybee will look for a .ddy file next to the .epw and extract all 99.6% and 0.4% design days. 
* ##### filter_ddays 
Boolean to note whether the design days in the ddy_file_ should be filtered to only include 99.6% and 0.4% design days. If None or False, all design days in the ddy_file_ will be incorporated into the sizing parameters. This can also be the integer 2 to filter for 99.0% and 1.0% design days. 
* ##### heating_fac 
A number that will get multiplied by the peak heating load for each zone in the model in order to size the heating system for the model. Must be greater than 0. (Default: 1.25). 
* ##### cooling_fac 
A number that will get multiplied by the peak cooling load for each zone in the model in order to size the cooling system for the model. Must be greater than 0. (Default: 1.15). 
* ##### eff_standard 
Text to specify the efficiency standard, which will automatically set the efficiencies of all HVAC equipment when provided. Note that providing a standard here will cause the OpenStudio translation process to perform an additional sizing calculation with EnergyPlus, which is needed since the default efficiencies of equipment vary dependingon their size. THIS WILL SIGNIFICANTLY INCREASE TRANSLATION TIME TO OPENSTUDIO. However, it is often worthwhile when the goal is to match the HVAC specification with a particular standard. The "HB Building Vintages" component has a full list of supported HVAC efficiency standards. You can also choose from the following. 

    * DOE_Ref_Pre_1980

    * DOE_Ref_1980_2004

    * ASHRAE_2004

    * ASHRAE_2007

    * ASHRAE_2010

    * ASHRAE_2013

    * ASHRAE_2016

    * ASHRAE_2019
* ##### climate_zone 
Text indicating the ASHRAE climate zone to be used with the efficiency_standard. When unspecified, the climate zone will be inferred from the design days. This input can be a single integer (in which case it is interpreted as A) or it can include the A, B, or C qualifier (eg. 3C). Typically, the "LB Import STAT" component can yield the climate zone for a particular location. 
* ##### bldg_type 
Text for the building type to be used in the efficiency_standard. If the type is not recognized or is None, it will be assumed that the building is a generic NonResidential. The following have meaning for the standard. 

    * NonResidential

    * Residential

    * MidriseApartment

    * HighriseApartment

    * LargeOffice

    * MediumOffice

    * SmallOffice

    * Retail

    * StripMall

    * PrimarySchool

    * SecondarySchool

    * SmallHotel

    * LargeHotel

    * Hospital

    * Outpatient

    * Warehouse

    * SuperMarket

    * FullServiceRestaurant

    * QuickServiceRestaurant

    * Laboratory

    * Courthouse

#### Outputs
* ##### sizing
Parameters with criteria for sizing the heating and cooling system. These can be connected to the "HB Simulation Parameter" component in order to specify settings for the EnergyPlus simulation. 