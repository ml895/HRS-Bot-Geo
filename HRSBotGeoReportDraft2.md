# High Rate Sedimentation - Bottom Geometry, Fall 2018
#### Kanha Matai (km694), Madeleine Lee (ml895)
#### 26 Oct 2018

## Abstract
The purpose of the High Rate Sedimentation (HRS) Bottom Geometry is to determine a method for eliminating or reducing the floc blanket decay currently occurring in sedimentation tanks in the lab. The team hopes to accomplish this by developing a new shape and geometry for the bottom of the sedimentation tube in order to maximize the reuse of large settling flocs.

## Introduction
The main challenge for the Bottom Geometry team is finding an optimal bottom geometry of the tube settler. The bottom geometry influences the density of the floc blanket, which is a dense layer of suspended flocs which allows particulates which have not coagulated, or coagulated particulates too small to settle, to attach onto the flocs which can be removed. Finding an optimal bottom geometry of the tube settler is vital to sedimentation because it can increase sedimentation efficiency by evening the floc blanket in the settler. Sedimentation is a crucial part of a water treatment plants as it acts as the major removal method for suspended and coagulated minerals, dirt and particles.

However, in the AguaClara lab, the floc blanket would initially form but decay with time. Thus, the performance of the system drastically decreased. After discussions regarding the differences between the design of the sedimentation tanks in the plants and in the lab, the High Rate Sedimentation: Bottom Geometry team was created to determine the optimal shape of the input of water into the sedimentation tubes in the lab to ensure the consistent formation of a stable floc blankets.

## Literature Review and Previous Work
One of the two teams that proposed changes in the bottom geometry of the tube settler was a previous high rate sedimentation team in the summer of 2018. They initially started with a flat bottom, but buildup was observed and was growing about half an inch in height every ten minutes. They then made a conical drilling in the bottom with the water inflow tube in the center. This still led to buildup of flocs at the bottom, which was hypothesized to be a result of a ring of flocs locking together in a circle that is bigger than the drilled hole, preventing resuspension of those flocs.

|Experiment|Upflow Velocity (mm/s)|Coagulant Dosage (mg/L)|Floc Blanket Formed|Ending Effluent Turbidity|Insights|
|:---:|:---:|:--------:|:---|:------|:---|
|[11](#experiment-11)|3|3.0|Yes|16 NTU|Faster floc blanket formation|
|[12](#experiment-12)|3|4.5|Yes|2-3 NTU &rarr; 11-12 NTU|Even faster floc blanket formation|
|[13](#experiment-13)|4|4.5|Yes|27-28 NTU|Gelling observed in flocculator and sedimentation tank|
|[14](#experiment-14)|4|4.5 <br/> with higher pump speed|Yes|~30 NTU|Gelling still observed; 4 mm/s may be too high|
|[15](#experiment-15)|3|4.5|Yes|27 NTU (at 1 hr)| With inserted, flat surfaced sedimentation tank bottom to observe floc buildup|
|[16](#experiment-16)|3|4.5|Yes|22 NTU|With conical sedimentation tank bottom, flocs are still building up|
**Table 1: Summary of HRS Summer 2018 experiment results**

The HRS Summer 2018 experiments confirm that an upflow velocity of 3 mm/s and a coagulant dosage of 4.5 mg/L are optimal parameters for high rate sedimentation; they also confirm that a flat and conical bottom cause floc buildup. These parameters are used in the current High Rate Sedimentation Team methods.

![Conical Insert 1](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/ConicalBottom.jpg)

![Conical Insert 1](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/conicalbottom2.png)

  **Figure 1: Conical filter insert by HRS Summer 2018.**

A previous Fluoride team proposed another change in the bottom geometry in which the bottom of the tube was cut at an angle and the bottom was closed except for a small part at the longest part of the tube for the inflow. The tube was essentially "squished" at the bottom such that the cross sectional areas are more rectangular than circular. This prevents flocs from locking together in a ring and causing buildup at the bottom. The stream of water broke up the buildup and allowed flocs to recirculate in the tube settler.

![Sliced tube bottom geometry](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/TriSedTank.jpeg)

  **Figure 2: Sliced tube bottom geometry by previous Fluoride team.**

## Methods
The main focus of the High Rate Sedimentation Bottom Geometry team was floc blanket stability through the modification of shape input of water into the tube settler. Hence, the independent variable of the experiments conducted by the team was the shape of the bottom and the dependent variable was the floc blanket performance and stability. Hence, critical controlled variables were the flow rate, shear, coagulant dose and influent turbidity.

The flow rate through the system was calculated in accordance to the desired up-flow velocity of 3mm/s, as determined by the work conducted by the HRS Summer 2018 team. As the tube settler had an inner diameter of 1 inch, using the formula dV/dt=pi*r^2*dh/dt, the flow rate of 90ml/min was set. The shear utilized was standardized with that of the HRS Summer 2018 team, and the majority of the AguaClara team, by utilizing the same flocculator as they were previously using. The coagulant dose of 7mg/L was chosen by the HRS Bottom Geometry team to ensure coagulant is not a limiting factor in the system. Finally, the influent turbidity chosen was 100 NTU which is the standardized influent turbidity for the AguaClara HRS teams.

The data utilized to compare and analyze the performance of the filter insert was  the effluent turbidity as it provided comparable values to determine the floc blanket performance and stability. The minimum effluent NTU would directly correlate with the performance, with lower values meaning better performance. Additionally, the time taken before the effluent NTU begins to increase after reaching peak performance would determine the floc stability. This would be a comparable measure for floc blanket stability as the longer it would take for the effluent to start increasing, the more stable the blanket is.

### Experimental Apparatus

  ![HRS Bottom Geometry Apparatus](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/ExperimentalApparatus.PNG)
**Figure 3: High Rate Sedimentation Fall 2018 Apparatus**

As shown in the Figure above, the overall experimental setup consists of a flocculator, clay and coagulant reservoirs, tube settler, and four distinct pumps. The first pump controls the water flow throughout the system with the flow rate set manually. The second pump is controlled by ProCoDa with the use of PID Control to dose clay into the system to create 100 NTU influent water. The third pump is used to control the coagulant dose and this too is set manually. The final pump is used to pump effluent out of the floc weir prevent the buildup of too many flocs. An additional pump is available, but not in use, to isolate the flowrate into the sedimentation tank.

### Procedure
Steps on how the HRS Bottom Geometry experimental apparatus was used are detailed below.

1. Use Python coagulant dosing calculation to determine the required coagulant pump speed for the desired coagulant dosage.
2. Check all valves and connections to make sure desired pathways are clear and undesired pathways are blocked.
3. Verify all influent, effluent and coagulant pumps are set to desired experimental flow rates.
4. Turn on influent pump to fill sedimentation tank with clean water.
5. Turn on clay stock stirrer if not already on.
6. Turn on influent and coagulant  pumps.
7. Set state to PID control in ProCoDA (this will turn on clay pump).

Throughout the experiments, the primary data collected and analyzed was the effluent turbidity.

###Designing Inserts
Design 1 - Symmetrical AguaClara Plant Design
As the issue of the unstable floc blanket was limited to the lab and not the actual AguaClara plant, the first design was inspired by the design of the AguaClara plant.
![Design of AguaClara Plant](https://github.com/AguaClara/HRS-Bot-Geo/blob/master/Images/AC%20Plant%20design.PNG?raw=true)
**Figure 4: Design of Sedimentation Tank in AguaClara Plants**

As seen through Figure 4, the AguaClara sedimentation tanks utilize two sloped surfaces to guide settling particles into the central high flow area. The off-centered input of water results in a difference in end results of the settling flocs. The flocs settled and sliding down the right slope would join the high inflow stream directed down, which is then directed up through the semicircle at the bottom and back into being resuspsended in the floc blanket. However, the flocs sliding the left side then collide with the flocs in the upward stream to form larger flocs to be resuspended in the blanket.

Inspired by this design, the HRS Bottom Geometry Team along with the Fluoride Auto Team designed the "Symmetrical AguaClara Plant Design."
![Symmetrical AguaClara Plant Design](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/fluoride%20auto%20insert.PNG)
**Figure 5: Filter insert with symmetrical, rectangular cross sections and a sloped top portion.**

As seen in Figure 5 above, this design closely resembled the AguaClara plant, with the primary difference having been the centered input. This decision was made primarily due to the design of the tube settler, as an off-centered insert would not align with the centered inflow tube at the bottom of the tube settler. Although the bottom of the design was a square due to complication in 3D drawing, this would then easily be modified once 3D printed by drilling.

Design 2 - Off-centered cone
Although the conical shape was tested by the HRS Summer 2018 team, the centered de

![Symmetrical AguaClara Plant Design](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/off%20center%20cone%20CAD.PNG)
![Symmetrical AguaClara Plant Design](https://raw.githubusercontent.com/AguaClara/HRS-Bot-Geo/master/Images/off%20center%20cone.PNG)
**Figure 6: Off-center conical insert with circular cross sections and water inlet at the tip.**

## Results and Analysis
Present an observation (results), then explain what happened (analysis).  Each paragraph should focus on one aspect of your results. In that same paragraph, you should interpret that result.  
In other words, there should not be two distinct paragraphs, but instead one paragraph containing one result and the interpretation and analysis of this result. Here are some guiding questions for results and analysis:

When describing your results, present your data, using the guidelines below:
* What happened? What did you find?
* Show your experimental data in a professional way.
```python
from aide_design.play import*
x = np.array([1,2,3,4,5])
y = np.array([1,2,3,4,5])
plt.figure('ax',(10,8))
plt.plot(x,y,'*')
plt.savefig('/Users/jillianwhiting/github/Jillian-Whiting/Images/linear')
plt.show()
```
![linear](https://github.com/jillianwhiting/Jillian-Whiting/blob/master/Images/linear.png?raw=true)
Figure 1: Captions are very important for figures. Captions go below figures.

After describing a particular result, within a paragraph, go on to connect your work to fundamental physics/chemistry/statics/fluid mechanics, or whatever field is appropriate. Analyze your results and compare with theoretical expectations; or, if you have not yet done the experiments, describe your expectations based on established knowledge. Include implications of your results. How will your results influence the design of AguaClara plants? If possible provide clear recommendations for design changes that should be adopted. Show your experimental data in a professional way using the following guidelines:
* Why did you get those results/data?
* Did these results line up with expectations?
* What went wrong?
* If the data do not support your hypothesis, is there another hypothesis that describes your new data?

## Conclusions
Explain what you have learned and how that influences your next steps. Why does what you discovered matter to AguaClara?

Make sure that you defend your conclusions with facts and results.

## Future Work
Describe your plan of action for the next several weeks of research. Detail the next steps for this team. How can AguaClara use what you discovered for future projects? Your suggestions for challenges for future teams are most welcome. Should research in this area continue?

## Bibliography
Logan, B. E., Hermanowicz, S. W., & Parker,A. S. (1987). A Fundamental Model for Trickling Filter Process Design. Journal (Water Pollution Control Federation), 59(12), 1029–1042.

# Manual
The goal of this section is to provide all of the guidance that would be necessary for a future team to pick up your work where you left off. Please try to be thorough and put yourselves in the shoes of a newcomer to the project. Below are some recommended sections, but the manual will likely take a slightly different form for each team.

## Fabrication Details
Include any information related to the fabrication of equipment, experimental apparatuses, or technologies. Include the purpose of each step and the fabrication methods used. Reference appropriate safety precautions.

## Special Components
If your subteam uses a particular part that is unique and you could foresee a future subteam needing to order it or learn more about it, please include basic information like the vendor where it was purchased, catalog/item number, and a link to any documentation.

## Experimental Methods
### Set-up
Step 1.
* Put tasks in a sequential order.
* It is okay to have sub-lists.
  - Like this.

### Experiment
Step 1.

### Cleaning Procedure
Step 1.

## Experimental Checklist
Another potential section could include a list of things that you need to check before running an experiment.

## ProCoDA Method File
Use this section to explain your method file. This could be broken up into several components as shown below:

### States
Here, you should describe the function of each state in your method file, both in terms of its overall purpose and also in terms of the details that make it distinct from other states. For example:
\begin{itemize}
\item \underline{OFF} - Resting state of ProCoDA. All sensors, relays, and pumps are turned off.
\end{itemize}

### Set Points
Here, you should list the set points used in your method file and explain their use as well as how each was calculated.

## Python Code

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

```python
# Comment
```
