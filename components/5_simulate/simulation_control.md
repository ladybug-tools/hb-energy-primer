# Simulation Control

![](../../.gitbook/assets/Simulation_Control.png)

![](../../.gitbook/assets/Simulation_Control%20%281%29.png) - [\[source code\]](https://github.com/ladybug-tools/honeybee-grasshopper-energy/blob/master/honeybee_grasshopper_energy/src//HB%20Simulation%20Control.py)

Create simulation controls with instructions for which types of EnergyPlus calculations to run.

## Inputs

* **do\_zone\_sizing**

  Boolean for whether the zone sizing calculation should be run. Default: True. 

* **do\_system\_sizing**

  Boolean for whether the system sizing calculation should be run. Default: True. 

* **do\_plant\_sizing**

  Boolean for whether the plant sizing calculation should be run. Default: True. 

* **for\_sizing\_period**

  Boolean for whether the simulation should be run for the sizing periods. Default: False. 

* **for\_run\_period**

  Boolean for whether the simulation should be run for the run periods. Default: True. 

## Outputs

* **sim\_control**

  A SimulationControl object that can be connected to the "HB Simulation Parameter" component in order to specify which types of EnergyPlus calculations to run. 

