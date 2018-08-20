### Wireless sensor network based pipeline failure detection system using non-intrusive relative pressure and differential temperature measurements

#### 0. Abstract

This paper describes the operation of a proposed non-intrusive relative pressure sensor, based on utilising low cost Force Sensitive Resistors \(FSR\). The paper also presents a novel method for detecting abnormal flow in pipes based on monitoring of the temperature differential between the pipe wall and its surroundings. The results showed that the calculated temperature differentials can be successfully used to detect abnormalities in the flow.

It is postulated that the differential temperature measurements in combination with relative pressure readings can be used to differentiate abnormal pressure drops caused by pipe failure from normal systematic or daily pressure variations.

#### 1. Introduction

* ##### Disadvantage

  * The challenges associated with the underground environment of these pipelines and the costs of installation and maintenance
  * the invasive nature of their sensing techniques
* ##### Various parameters\(the health of the buried water distribution networks\)

  1. vibrations\(振动\)
  2. flow
  3. pressure
  4. soil water content
  5. strain
  6. corrosion
* ##### main reasons for a fluctuation of pressure in the pipes

  1. fluctuations in demand
  2. intentional systematic pressure
  3. pressure transients（瞬间压力）
  4. pipe failure\*
* ##### why

  * Faults in the pipeline will affect the internal pressure of the pipes.Therefore, internal pressure is a suitable indirect indicator for assessing the operational and structural integrity of the pipes.
* ##### the core of introduction

  * a novel nonintrusive relative pressure sensor based on utilising low cost Force Sensitive Resistors
  * monitoring the temperature difference between the pipe wall and its surroundings and relative pressure sensors in order to detect pipe failure

#### 2. Theory of operation

* ##### Theory

  * As the internal pressure of a pipe changes the internal stress applied to the pipe wall will also change,the proposed sensing system indirectly uses this change in the radius to detect the changes of the internal pressure of the pipe.
* ##### Schematic of the relative pressure sensor assembly

  * The proposed relative pressure sensor assembly is composed of a stainless steel clip.As the change in the contact force is caused by the change in the internal pressure of the pipe the output of the FSR sensor can be related to the change in the pressure of the pipe.

    ![](/assets/8201.jpg)

    ###### Figure 1. Schematic of the relative pressure sensor assembly
* ##### Equation

  * Equation 1 can be used to estimate the contact pressure PC between the pipe and the clip.
  
  $$
  Pc=  (P.r_p^2.E_j.t_j)/((r_p^2.E_j.t_j)+(r_j^2.E_p.t_p))------Equation 1
  $$
  
Where $$P$$ is the internal pressure in the pipe; $$r_j$$and $$r_p$$ are the radii of the clip and the pipe; $$Ej$$ and $$E_p$$ are the respective material Young’s modulii of elasticity of the clip and pipe and $$t_j$$ and $$t_p$$ are the thickness of the clip and pipe respectively. 

* ##### the effect of pipe geometry on the applied contact pressure on the sensor 
 - Figure 2 and Figure 3 show the effect of pipe geometry on the applied contact pressure on the sensor for medium density polyethylene \(MDPE\) and cast iron pipes \(at 1 kPa\) respectively.
![](/assets/8202.jpg)
###### Figure 2. Effect of geometry on the applied force for MDPE pipes 
![](/assets/8203.jpg)                                                                                            
###### Figure 3. Effect of geometry on the applied force for Cast-iron pipes

- ##### FSR Sensor Conclusion
  - Comparing the effect of the pipe material on the applied force on the sensor indicates that
the proposed sensor in its current form is more suited for use on plastic pipes.
  -  the design parameters of the sensor assembly can be modified for metallic pipes
- ##### Temperature Conclusion
  - why: A change in the speed of the flow in the pipe results in the change in the residence time of the water in the pipe, which results in the heating/cooling effect of the medium on the pipe wall
  - Propose: Temperature differential between the pipe wall and the surrounding soil can be potentially used as an indicator of sudden changes in the flow within the pipe.

#### 3. Test Setup
The FSR based relative pressure sensors were deployed on plastic and metallic pipes at an industrial leak test facility to investigate their performance.Figure 4 shows the setup of the sensors deployed in these trials.
![](/assets/8204.jpg)
###### Figure 4.  Setup of the sensors on the plastic pipe
Ultra low power wireless sensor nodes were also deployed during these trials.A 1W solar panel was also placed on the top of the post in order to charge the battery.The nodes were connected to the sensors attached tothe pipe under the ground via a multicore twisted pair cable.These measurements were transmitted wirelessly to a mother node,which was placed inside a building close to the nodes.The sensors were monitored for a period of approximately 6 months.Figure 5 illustrates the schematic of the setup of the node and the sensors attached to the pipe.


![](/assets/8205.jpg)
###### Figure 5. Schematic of the sensors and the nodes

#### 4. Result and discussion
Figure 6 shows a 20 day period of the data collected by one of the nodes installed on the plastic pipe.Figure 6 shows that systematic pressure changes were also registered by the FSR sensors (10th and 16th July).
![](/assets/8206.jpg)
###### Figure 6. Relative pressure and temperature readings for a period of 20 days associated with the plastic pipe
Figure 7 illustrates relative pressure and calculated absolute temperature differential(between pipe and soil) for a 6 day period where, during the first three days and the last day, valve training was carried out at the test facility.The drop in the temperature of the pipe wall was not present in the temperature readings from the sensors placed within the soil adjacent to the pipe, leading to an abnormality in the temperature differential as seen in Figure 7. 
![](/assets/8207.jpg)
###### Figure 7. Temperature differential and relative pressure readings for a period of 5 day
- ##### why:
  - Sudden change in the temperature of the pipe wall was caused by the sudden increase in flow
  - Poor thermal conductivity of the soil this change in temperature 
- ##### Test Conclusion
  - the relative pressure readings in combination with temperature differentials to be used for the detection of pipe failures and to differentiate them from normal variations
  - Advantage: This removes the need for time consuming and costly precision calibration processes
- ##### My opinion
  - 由于土壤的热导热性较差，故本次实验的相对温度变得并不是很有意义，变成单方面的管壁温度下降。
  - 如果出现真正的泄漏，应该会有水渗出，导致土壤含水量变化，进而导致土壤温度下降，这时模拟较为有意义。
  - 但是如果出现土壤温度下降，管壁温度也下降，则相对温度就与平常的相对温度差别不大（需进一步验证）

Figure 8 and Figure 9show the daily range of the relative pressure and theabsolute daily range of the temperature differential for the 5 day period presented in Figure 7 respectively.The dotted lines represents the threshold for detection of abnormality.
![](/assets/8208.jpg)
###### Figure 8. Daily range of the relative pressure
![](/assets/8209.jpg)
###### Figure 9. Absolute daily range of the temperature differential
A fixed or adaptive thresholds could be used to flag abnormal events in the pipe.And learning algorithms could be trained using the processed data for each network based on the operational characteristics of that network which can potentially provide better accuracy in detection of pipe failure events.
 - Learning Algorithms Method
   - 线性回归
   - k-means
   - SVM
   - neural network

### 5. Conclusions
- ##### A FSR based relative pressure sensor
- ##### A wireless sensor node
- ##### The differential temperature measurements in combination with relative pressure readings can be used to differentiate abnormal pressure drops caused by pipe failure from
normal systematic or daily pressure variations





