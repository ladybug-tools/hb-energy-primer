## Adaptive Comfort Map

![](../../images/components/Adaptive_Comfort_Map.png)

![](../../images/icons/Adaptive_Comfort_Map.png) - [[source code]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Adaptive%20Comfort%20Map.py)


Compute spatially-resolved operative temperature and adaptive thermal comfort from a Honeybee model. 

This recipe uses EnergyPlus to obtain longwave radiant temperatures and indoor air temperatures. The outdoor air temperature and air speed are taken directly from the EPW. A Radiance-based, enhanced 2-phase method is used for shortwave MRT calculations, which uses an accurate direct sun calculation with precise solar positions. 

The energy properties of the model geometry are what determine the outcome of the simulation, though the model's Radiance sensor grids are what determine where the comfort mapping occurs. 



#### Inputs
* ##### model [Required]
A Honeybee Model for which adaptive comfort will be mapped. Note that this model should have radiance grids assigned to it in order to produce meaningful results. 
* ##### epw [Required]
Path to an EPW weather file to be used for the comfort map simulation. 
* ##### ddy [Required]
Path to a DDY file with design days to be used for the initial sizing calculation of the energy simulation. 
* ##### north 
A number between -360 and 360 for the counterclockwise difference between the North and the positive Y-axis in degrees. This can also be Vector for the direction to North. (Default: 0). 
* ##### run_period 
An AnalysisPeriod to set the start and end dates of the simulation. If None, the simulation will be annual. 
* ##### sensor_count 
Integer for the maximum number of sensor grid points per parallel execution. (Default: 200). 
* ##### air_speed 
A single number for air speed in m/s or an hourly data collection of air speeds that align with the input run_period_. This will be used for all indoor comfort evaluation. Note that the EPW wind speed will be used for any outdoor sensors. (Default: 0.1). 
* ##### comfort_par 
Optional comfort parameters from the "LB Adaptive Comfort Parameters" component to specify the criteria under which conditions are considered acceptable/comfortable. The default will use ASHRAE-55 adaptive comfort criteria. 
* ##### solar_body_par 
Optional solar body parameters from the "LB Solar Body Parameters" object to specify the properties of the human geometry assumed in the shortwave MRT calculation. The default assumes average skin/clothing absorptivity and a human subject always has their back to the sun at a 45-degree angle (SHARP = 135). 
* ##### radiance_par 
Text for the radiance parameters to be used for ray tracing. (Default: -ab 2 -ad 5000 -lw 2e-05). 
* ##### run_settings 
Settings from the "HB Recipe Settings" component that specify how the recipe should be run. This can also be a text string of recipe settings. 
* ##### run [Required]
Set to True to run the recipe and get results. This input can also be the integer "2" to run the recipe silently. 

#### Outputs
* ##### report
Reports, errors, warnings, etc. 
* ##### op_temp
A folder containing CSV maps of Operative Temperature for each sensor grid at each time step of the analysis. This can be connected to the "HB Read Thermal Matrix" component to parse detailed results into Grasshopper. Values are in Celsius. 
* ##### condition
A folder containing CSV maps of comfort conditions for each sensor grid at each time step of the analysis. This can be connected to the "HB Read Thermal Matrix" component to parse detailed results into Grasshopper. Values are as follows. 

    * -1 = unacceptably cold conditions

    *  0 = neutral (comfortable) conditions

    * +1 = unacceptably hot conditions
* ##### deg_neut
A folder containing CSV maps of the degrees Celsius from the adaptive comfort neutral temperature for each sensor grid at each time step of the analysis. This can be connected to the "HB Read Thermal Matrix" component to parse detailed results into Grasshopper. This can be used to understand not just whether conditions are acceptable but how uncomfortably hot or cold they are. 
* ##### TCP
Lists of values between 0 and 100 for the Thermal Comfort Percent (TCP). These can be plugged into the "LB Spatial Heatmap" component along with meshes of the sensor grids to visualize spatial thermal comfort. TCP is the percentage of occupied time where thermal conditions are acceptable/comfortable. Occupied hours are determined from the occupancy schedules of each room (any time where the occupancy schedule is >= 0.1 will be considered occupied). Outdoor sensors are considered occupied at all times. More custom TCP studies can be done by post-processing the condition results. 
* ##### HSP
Lists of values between 0 and 100 for the Heat Sensation Percent (HSP). These can be plugged into the "LB Spatial Heatmap" component along with meshes of the sensor grids to visualize uncomfortably hot locations. HSP is the percentage of occupied time where thermal conditions are hotter than what is considered acceptable/comfortable. Occupied hours are determined from the occupancy schedules of each room (any time where the occupancy schedule is >= 0.1 will be considered occupied). Outdoor sensors are considered occupied at all times. More custom HSP studies can be done by post-processing the condition results. 
* ##### CSP
Lists of values between 0 and 100 for the Cold Sensation Percent (CSP). These can be plugged into the "LB Spatial Heatmap" component along with meshes of the sensor grids to visualize uncomfortably cold locations. CSP is the percentage of occupied time where thermal conditions are colder than what is considered acceptable/comfortable. Occupied hours are determined from the occupancy schedules of each room (any time where the occupancy schedule is >= 0.1 will be considered occupied). Outdoor sensors are considered occupied at all times. More custom CSP studies can be done by post-processing the condition results. 