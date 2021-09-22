##### Table of Contents  
[About the Project](#project)  
[Implementation Logical Description](#logic)  
[Adress Table](#addressing)

# Sorting Station

<a name="project"/>

## About the Project
In this work, an application is implemented in Ladder, simulated in [Siemens's TIA Portal V15](https://new.siemens.com/global/en/products/automation/industry-software/automation-software/tia-portal.html?gclid=Cj0KCQjwqKuKBhCxARIsACf4XuFAMB-0TO1Dr0LAtD0IdDRiWIuuLU7WvIdBNcHoMLemTrMuXtZVnvYaAtS3EALw_wcB) for a sorting station modelled by [Factory IO](https://factoryio.com/), in order to sort material of different colors to their respective ramps.

<p align="center">
<img width="400" height="300" src=https://github.com/Vangasse/sorting_station/blob/main/img/Sorting%20Station.png>
</p>

<p align="center"> 
<b>Figure 1:</b> Sorting Station.
</p>

Three types of material are considered, Green, Gray and Blue, which are identified by the Vision Sensor ilustrated in Figure 2. Then led through the conveyors to the ramps 1(Green), 2(Gray) and 3(Blue), in Figure 3, by the triggering of the sorters at the top of the image.

<p align="center">
<img width="200" height="300" src=https://github.com/Vangasse/sorting_station/blob/main/img/Vision%20Sensor.png>
</p>

<p align="center"> 
<b>Image 2:</b> Vision Sensor.
</p>

<p align="center">
<img width="400" height="300" src=https://github.com/Vangasse/sorting_station/blob/main/img/Ramps.png>
</p>

<p align="center"> 
<b>Image 3:</b> Ramps 1, 2 and 3 from right to left and Sorters 1, 2 and 3, also from right to left.
</p>

The user can start the process by pressing the green Start button at the left of Figure 4, and to stop it, the red Stop button at the center of the same figure is available.

<p align="center">
<img width="250" height="300" src=https://github.com/Vangasse/sorting_station/blob/main/img/Automation%20Cabinet.png>
</p>

<p align="center"> 
<b>Image 4:</b> Automation Cabinet with Start button in green at left and Stop button in red at center implemented.
</p>

<a name="logic"/>

## Implementation Logical Description

<a name="addressing"/>

## Adress Table

The table below contains the compontent adresses used in the implementation.

| Artifact        | Type | Address |
| -------------   |:----:| -------:|
|                 | Bool |  %I0.0  |
| Start           | Bool |  %I0.1  |
| Stop            | Bool |  %I0.3  |
|                 | Bool |  %I0.7  |
| Vision Sensor   | DInt |  %ID30  |
|                 | DInt |  %ID31  |
|                 | DInt |  %ID32  |
| Entry Conveyor  | Bool |  %Q0.0  |
| Exit Conveyor   | Bool |  %Q0.2  |
| Sorter 1 Turn   | Bool |  %Q0.3  |
| Sorter 1 Belt   | Bool |  %Q0.4  |
| Sorter 2 Turn   | Bool |  %Q0.5  |
| Sorter 2 Belt   | Bool |  %Q0.6  |
| Sorter 3 Turn   | Bool |  %Q0.7  |
| Sorter 3 Belt   | Bool |  %Q1.0  |
| Timmer 1 Valve  | Bool |  %Q1.4  |
| Timmer 2 Valve  | Bool |  %Q1.5  |
| Timmer 3 Valve  | Bool |  %Q1.6  |




