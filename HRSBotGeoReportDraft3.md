# High Rate Sedimentation - Bottom Geometry, Fall 2018
#### Kanha Matai (km694), Madeleine Lee (ml895)
#### 16 Nov 2018

## Abstract
The purpose of the High Rate Sedimentation (HRS) Bottom Geometry is to determine a method for eliminating or reducing the floc blanket decay currently occurring in sedimentation tanks in the lab. The team hopes to accomplish this by developing a new shape and geometry for the bottom of the sedimentation tube in order to maximize the reuse of large settling flocs.

## Introduction

The High Rate Sedimentation: Bottom Geometry Team was created to improve sedimentation, which is a crucial part of the water treatment process as it acts as the major removal method for suspended and coagulated minerals, dirt and particles. The main challenge for the Bottom Geometry Team is finding an optimal bottom geometry of the tube settler to prevent sediment buildup at the bottom. Although the sediment buildup does not affect sedimentation efficiency, this buildup should be avoided to make the cleaning of the apparatus easier. The bottom geometry influences the density of the floc blanket, a dense layer of suspended flocs to which small or uncoagulated particles can attach and subsequently be removed.

However, in the AguaClara lab, the floc blanket would initially form but decay with time, so the performance of the system drastically decreased. After discussions regarding the differences between the design of the sedimentation tanks in the plants and in the lab, the High Rate Sedimentation: Bottom Geometry team was created to determine the optimal shape of the input of water into the sedimentation tubes in the lab to ensure the consistent formation of a stable floc blankets.

## Literature Review and Previous Work
A previous High Rate Sedimentation Team proposed changes to the bottom geometry of the tube settler in the summer of 2018. The tube settler initially had a flat bottom, but buildup was observed and was growing about half an inch in height every ten minutes. They then made a conical drilling in the bottom with the water inflow tube in the center. This still led to buildup of flocs at the bottom, which was hypothesized to be a result of a ring of flocs locking together in a circle that is bigger than the drilled hole, preventing resuspension of those flocs.

**Table 1: Summary of HRS Summer 2018 experiment results**

|Experiment|Upflow Velocity (mm/s)|Coagulant Dosage (mg/L)|Floc Blanket Formed|Ending Effluent Turbidity|Insights|
|:---:|:---:|:--------:|:---|:------|:---|
|[11](#experiment-11)|3|3.0|Yes|16 NTU|Faster floc blanket formation|
|[12](#experiment-12)|3|4.5|Yes|2-3 NTU &rarr; 11-12 NTU|Even faster floc blanket formation|
|[13](#experiment-13)|4|4.5|Yes|27-28 NTU|Gelling observed in flocculator and sedimentation tank|
|[14](#experiment-14)|4|4.5 <br/> with higher pump speed|Yes|~30 NTU|Gelling still observed; 4 mm/s may be too high|
|[15](#experiment-15)|3|4.5|Yes|27 NTU (at 1 hr)| With inserted, flat surfaced sedimentation tank bottom to observe floc buildup|
|[16](#experiment-16)|3|4.5|Yes|22 NTU|With conical sedimentation tank bottom, flocs are still building up|

The HRS Summer 2018 experiments confirm that an upflow velocity of 3 mm/s and a coagulant dosage of 4.5 mg/L are optimal parameters for high rate sedimentation; they also confirm that a flat and conical bottom cause floc buildup. These parameters are used in the current High Rate Sedimentation Team methods.

![Conical Insert 1](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/ConicalBottom.jpg)

![Conical Insert 1](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/conicalbottom2.png)

**Figure 1: Conical filter insert by HRS Summer 2018. **

A previous Fluoride team proposed another change in the bottom geometry in which the bottom of the tube was cut at an angle and the bottom was closed except for a small part at the longest part of the tube for the inflow. The tube was essentially "squished" at the bottom such that the cross sectional areas are more rectangular than circular. This prevents flocs from locking together in a ring and causing buildup at the bottom. The stream of water broke up the buildup and allowed flocs to recirculate in the tube settler.

![Sliced tube bottom geometry](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/TriSedTank.jpeg)

**Figure 2: Sliced tube bottom geometry by previous Fluoride team. Click [this link](https://www.youtube.com/watch?v=EajLuP6eX9w&feature=youtu.be) for a video of the sedimentation tank.**

## Methods
The main focus of the High Rate Sedimentation Bottom Geometry team was floc blanket stability through the modification of shape input of water into the tube settler. Hence, the independent variable of the experiments conducted by the team was the shape of the bottom and the dependent variable was the floc blanket performance and stability. Hence, critical controlled variables were the flow rate, coagulant dose and influent turbidity.

The flow rate through the system was calculated in accordance to the desired up-flow velocity of 3mm/s, as determined by the work conducted by the HRS Summer 2018 team. As the tube settler had an inner diameter of 1 inch, using the formula dV/dt=pi*r^2*dh/dt, the flow rate of 90ml/min was set. The coagulant dose of 4.2mg/L was chosen by the HRS Bottom Geometry team to ensure coagulant is not a limiting factor in the system. Finally, the influent turbidity chosen was 100 NTU which is the standardized influent turbidity for the AguaClara HRS teams.

The data utilized to compare and analyze the performance of the filter insert was the effluent turbidity as it provided comparable values to determine the floc blanket performance and stability. The minimum effluent NTU would directly correlate with the performance, with lower values meaning better performance. Additionally, the floc blanket stability would be determined by the time it takes for the effluent turbidity to start increasing after reaching the maximum removal, as the longer the time it takes for the turbidity to increase, the more stable the blanket would be.

### Experimental Apparatus

  ![HRS Bottom Geometry Apparatus](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/ExperimentalApparatus.PNG)

**Figure 3: High Rate Sedimentation Fall 2018 Apparatus**

As shown in the Figure above, the overall experimental setup consists of a flocculator, clay and coagulant reservoirs, tube settler, and four distinct pumps. The first pump controls the water flow throughout the system with the flow rate set manually. The second pump is controlled by ProCoDa with the use of PID Control to dose clay into the system to create 100 NTU influent water. The third pump is used to control the coagulant dose and this too is set manually. The final pump is used to pump effluent out of the floc weir prevent the buildup of too many flocs.

### Procedure
The procedure of setting up the HRS Bottom Geometry experimental apparatus is detailed below.

1. Use Python coagulant dosing calculation to determine the required coagulant pump speed for the desired coagulant dosage.
2. Check all valves and connections to make sure desired pathways are clear and undesired pathways are blocked.
3. Verify all influent, effluent and coagulant pumps are set to desired experimental flow rates.
4. Turn on influent pump to fill sedimentation tank with clean water.
5. Turn on clay stock stirrer if not already on.
6. Turn on influent and coagulant pumps.
7. Set state to PID control in ProCoDA (this will turn on clay pump).

Throughout the experiments, the primary data collected and analyzed was the effluent turbidity. This was measured automatically by ProCoDa and logged into an excel file for analysis once the experiment is over.

### Designing Inserts
Design 1 - Symmetrical AguaClara Plant Design

As the issue of the unstable floc blanket was limited to the lab and not the actual AguaClara plant, the first design was inspired by the design of the AguaClara plant.

![Design of AguaClara Plant](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/AC%20plant%20filter.PNG)

**Figure 4: Design of Sedimentation Tank in AguaClara Plants**

As seen in Figure 4, the AguaClara sedimentation tanks utilize two sloped surfaces to guide settling particles into the central high flow area. The off-centered input of water results in a difference in end results of the settling flocs. The flocs that slide down the slope on the right would join the high inflow stream directed down, which are subsequently directed up through the semicircle at the bottom and become resuspsended in the floc blanket. However, the flocs sliding down left side would collide with the flocs in the upward stream to form larger flocs to be resuspended in the blanket.

Inspired by this design, the HRS Bottom Geometry Team along with the Fluoride Auto Team designed the "Symmetrical AguaClara Plant Design."

![Symmetrical AguaClara Plant Design](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/fluoride%20auto%20insert.PNG)

**Figure 5: Filter insert with symmetrical, rectangular cross sections and a sloped top portion.**

As seen in Figure 5 above, this design closely resembled the AguaClara plant, with the primary difference having been the centered input. This decision was made primarily due to the design of the tube settler, as an off-centered insert would not align with the centered inflow tube at the bottom of the tube settler. Although the bottom of the design was a square due to complication in 3D drawing, this would then easily be modified once 3D printed by drilling.

Design 2 - Off-centered Cone

Although the conical shape was tested by the HRS Summer 2018 team, the centered design still caused a buildup of flocs. The off-center conical shape most closely resembles the sliced tube filter designed by a previous Fluoride team. If the water inflow comes from the side of the tube, it can break up the rings of flocs that would have otherwise collected near the bottom. This exactly conical design would not be practical to insert into the tube settler, so a new design was created to make testing easier. The new design is shaped like a regular cylinder, but the hollow part of the cylinder is shaped like an off-center cone, and there is an open hole for the water inlet.

![Symmetrical AguaClara Plant Design](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/off%20center%20cone%20CAD.PNG)
![Symmetrical AguaClara Plant Design](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/off%20center%20cone.PNG)
![Symmetrical AguaClara Plant Design](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/off%20center%20cone%20in%20cylinder%20CAD.PNG)

**Figure 6: Off-center conical insert with circular cross sections and water inlet at the tip.**

## Results and Analysis
The first experiment run by the Bottom Geometry team was the baseline control experiment at 3mm/s upflow speed.

![Failed Control Experiment](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/Baseline%20Attempt.PNG)
**Figure 7: Graph of failed control experiment with high effluent turbidity.**

As seen in the graph, the turbidity of the effluent lies between 30 NTU and 60 NTU for the first 5.25 hours. In the beginning before the first hour, a floc blanket formed and stabilized. However, the blanket began to decay fairly quickly, which is indicated by the rapid increase of effluent turbidity. Upon closer analysis, it was found that the improper calibration of the pumps caused the floc blanket to fail due to excessively high flowrate through the system. Hence, another trial was set with the recalibrated pump.

![Successful Experiment of 3mm](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/3mm%20original%20flocc.PNG)
**Figure 8: Graph of 3 mm/s upflow velocity.**

In this experiment, a stable floc blanket formed with a consistant effluent turbidity of below 5 NTU. Although the floc blanket appeared unstable, the experiment had a long run time of 14 hours and the effluent turbidity stayed below 10 NTU. Additionally, decay was linear as opposed to exponential decays observed in previous semesters. Compared to the results of the previous HRS teams' experiments, the blanket formed was more stable and efficient. The summer 2018 team was able to produce a blanket at 3 mm/s upflow velocity, but they were not able to produce one at 2 mm/s upflow velocity. Hence, a trial was set to compare the performance at 2mm/s upflow velocity between the Bottom Geometry system and the HRS Summer 2018 results.

Below are the results from the experiment run with an upflow velocity of 2 mm/s.
![2mm Successful Experiment](https://github.com/AguaClara/HRS-Bot-Geo/blob/master/Images/2mm%20original%20flocc.PNG?raw=true)
**Figure 9: 2mm/s Upflow velocity trial**

In this experiment, a floc blanket formed with consistent removal of 2-4 NTU. Additionally, there was no floc blanket decay as the effluent NTU remained constant throughout the trial. The increase in turbidity at the end of the figure was contributed to the finishing of clay stock, not the decay of the blanket itself. This result strongly contradicts that obtained by the HRS Summer 2018 team, as the Bottom Geometry team was able to form a blanket at 2mm/s. Additionally, results also contradicted observations by the previous few HRS teams, as the floc blanket did not decay. After comparing the lab setup between the apparatus with that of the Summer and previous semester teams, the Bottom Geometry team believed the difference would be attributed to the difference in flocculators, as other components appeared identical. Hence, a trial was set up to compare whether the flocculator would impact the floc blanket formation.

![Flocculator Comparison](https://github.com/AguaClara/HRS-Bot-Geo/blob/master/Images/2mm%20flocc%20comparison.PNG?raw=true)
**Figure 10: Flocculator comparison**

In this figure, the effluent turbidity from the 2mm/s upflow velocity trial was plotted with the effluent turbidity at 2mm/s upflow velocity, but using the flocculator utilized by the HRS Summer 2018 team and the current HRS Floc Recycle team. The blue date indicates the results from figure 9 with the red data representing the date from the HRS Summer 2018 and Floc Recycle flocculator. From this data, the Bottom Geometry team could not attribute the variance in filter performance between the Bottom Geometry apparatus and previous HRS teams was caused by the flocculator. However, the team was able to conclude that the stability of filter was due to the buildup of flocs as opposed to a stable floc blanket.
![Floc buildup](https://github.com/AguaClara/HRS-Bot-Geo/blob/master/Images/Floc%20buildup.PNG?raw=true)
**Figure 11: Floc Buildup**

From the figure above, the Bottom Geometry was able to deduce that the stability was contributed due to the stationary buildup of flocs in the sedimentation tank. This acted similar to a floc blanket, with channels that allowed for smaller scaled flocs to pass through the large channels and get removed. Additionally, a dense floc blanket with actual suspended particles was positioned above the floc buildup, thus improving the filter efficiency. Although this filter worked efficiently and was stable, this performance cannot be carried forward into AguaClara plants as floc buildup would increase the required maintenance time and down time for the filter as these settled particles can only be removed manually. However, the next step for the Bottom geometry team was to determine whether similar buildup was occuring at 3mm/s upflow velocity.

## Conclusions
Explain what you have learned and how that influences your next steps. Why does what you discovered matter to AguaClara?

Make sure that you defend your conclusions with facts and results.

## Future Work
Describe your plan of action for the next several weeks of research. Detail the next steps for this team. How can AguaClara use what you discovered for future projects? Your suggestions for challenges for future teams are most welcome. Should research in this area continue?

## Bibliography
AWWA/ASCE (2012).Water Treatment Plant Design.*Water Treatment Plant Design*. McGraw Hill,New York,fifth edition.

Carissimi, E., Miller, J., and Rubio, J.   (2007). Characterization of the high kinetic energy dissipation of the Flocs Generator Reactor (FGR) - ScienceDirect.

Galantino, C. and Kang, A. (2017).  High Rate Sedimentation, Summer 2017 - Overleaf.

Garland,  C.,  Weber-Shirk,  M.,  and  Lion,  L.  W.  (2017).   Revisiting  Hydraulic  Flocculator  Design  for Use  in  Water  Treatment  Systems  with  Fluidized  Floc  Beds. *Environmental  Engineering  Science*,34(2):122-129.

Kawamura, S. (1991).*Integrated Design and Operation of Water Treatment Facilities*.  Second edition.

O'Melia,  C.R.  (1972). Coagulation  and Flocculation: Physicochemical  Processes  for  Water  Quality Control,.

Pennock,  W.  H.,  Chan, F.  C.,  Weber-Shirk,  M.  L., and  Lion,  L.  W.  (2016). Theoretical Foundation and  Test  Apparatus  for an  Agent-Based  Flocculation Model. *Environmental  Engineering  Science*,33(9):688{698.

Swetland, K. A., Weber-Shirk, M. L., and Lion, L. W. (2014). Flocculation-Sedimentation Performance Model for Laminar-Flow Hydraulic Flocculation with Polyaluminum Chloride and Aluminum Sulfate Coagulants. *Journal of Environmental Engineering*, 140(3):04014002.

# Manual

## Experimental Methods

The following is a general outline of tasks to be done prior, during, and after experimentation. ProCoDA is a software that is used extensively during experiments; the software allows the user to automate data collection and various components of the experimental apparatus. PID stands for proportional integral derivative and is calibrated to control the clay pump via ProCoDA.

 1. Drain the sedimentation tank and flocculator from previous experimental trial, if necessary.
 2. Refill clay and coagulant stock tanks.
 3. Run tap water through the system to rinse the flocculator, sedimentation tank, and connecting piping.
 4. Rinse and refill turbidimeters.
 5. Use Python coagulant dosing calculation to determine the required coagulant pump speed for the desired coagulant dosage.
 6. Check all valves and connections to make sure desired pathways are clear and undesired pathways are blocked.
 7. Verify all influent, effluent and coagulant pumps are set to desired experimental flow rates.
 8. Turn on influent pump to fill sedimentation tank with clean water.
 9. Plug in clay stock stirrer if not already plugged in.
 10. Turn on influent, effluent, and coagulant pumps.
 11. Set state to PID control in ProCoDA (this will turn on clay pump and also turn on data collection).
 12. After the experiment has run for the desired runtime, Set ProCoDa state to OFF, and turn of the water pump and coagulant pump.

### States
The sole state utilized was the PID control state, which controled the clay pump rpm The values of P, i, D were calibrated using this guide https://confluence.cornell.edu/display/AGUACLARA/Calibrating+PID+Control. The Turb Target is set at 100 NTU for all experiments as it is convention for this series of experiments.

The water pump is also controlled by ProCoDA. Whereas, the pump after the sedimentation tank is controlled manually and is set at 60 rpm to maintain a 2 mm/s upflow velocity through the sedimentation tank.
### Set Points

| Set Point             | Setting |
|:--------------------- |:------- |
| Turb Target           | 100     |
| P                     | 68      |
| i                     | 125     |
| D                     | 0       |
| Influent Turbidty ID  | 1       |
| Effluent Turbidity ID | 2       |
| Floc removal time     | 10      |
| Run time              | 3590    |
| Fast pump             | 0.5     |
| Normal pump           | 0.12    |


## Python Code
Calculations were done in Python to determine PaCl coagulant dosing parameters and flocculator design parameters in order to run experiments and construct experimental apparatus.

###PaCl Dosing Calculations

The calculation logic for determining the coagulant dosing are derived from Dr. Monroe Weber-Shirk's CEE 4540 Lecture notes.

```Python
## PACl Dosing

from aide_design.play import*

#inputs
C_sys = 4.2*(u.mg/u.L)         #C_sys is the desired concentration of coagulant in the system
C_labstock = 70.28*(u.g/u.L)   #C_labstock is the concentration of coagulant in the stock
Q_sys = 1*(u.mL/u.s)           #Q_sys is the flow rate of the system
K_dilution = 5*(u.mL/u.L)      #K_dilution is the volume of coagulant per liter of distilled water
V_reservoir = 5*(u.L)          #V_reservoir is the volume of the coagulant stock tank in the system
Frac_reservoir = .76
Q_per_rpm = .00195 *(u.mL/u.s) #Q_per_rpm is the coagulant pump flow rate per rpm

#Calculations
M_flow_coag = (Q_sys * C_sys).to(u.mg/u.s)  
C_reservoir = (C_labstock * K_dilution).to(u.gram/u.L)
Q_reservoir = (M_flow_coag / C_reservoir).to(u.mL/u.s)
V_lab = ((V_reservoir * C_reservoir) / C_labstock).to(u.L)

#Outputs
RPM = Q_reservoir / Q_per_rpm                                       #RPM is the RPM required for coagulant dosage
RunTime = ((V_reservoir * Frac_reservoir) / Q_reservoir).to(u.hour) #RunTime is the run time of the system

print('The RPM needed for this coagulant dosage is' ,RPM)

print('The run time is ', RunTime)
```

### Variables
$g$: gravity
$\sigma$: dispersion
$a$: amplitude
$h$: water depth
$H$: distance from wave crest to trough (2$a$)
$T$: wave period
$\lambda$: wavelength
$k$: wavenumber
$c_p$: celerity (wave phase speed)
$P$: pressure
$F$: force
$u$, $w$: x-velocity, z-velocity components
