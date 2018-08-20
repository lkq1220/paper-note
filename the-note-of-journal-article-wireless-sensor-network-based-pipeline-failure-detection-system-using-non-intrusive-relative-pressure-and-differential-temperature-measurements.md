### Wireless sensor network based pipeline failure detection system using non-intrusive relative pressure and differential temperature measurements

#### 0. Abstract
This paper describes the operation of a proposed non-intrusive relative pressure sensor, based on utilising low cost Force Sensitive Resistors (FSR). The paper also presents a novel method for detecting abnormal flow in pipes based on monitoring of the temperature differential between the pipe wall and its surroundings. The results showed that the calculated temperature differentials can be successfully used to detect abnormalities in the flow.

It is postulated that the differential temperature measurements in combination with relative pressure readings can be used to differentiate abnormal pressure drops caused by pipe failure from normal systematic or daily pressure variations.

#### 1. Introduction
- ##### Disadvantage 
  - The challenges associated with the underground environment of these pipelines and the costs of installation and maintenance
  - the invasive nature of their sensing techniques
- ##### Various parameters(the health of the buried water distribution networks)
  1. vibrations(振动)
  2. flow
  3. pressure
  4. soil water content
  5. strain
  6. corrosion
- ##### main reasons for a fluctuation of pressure in the pipes 
  1. fluctuations in demand
  2. intentional systematic pressure
  3. pressure transients（瞬间压力）
  4. pipe failure*
- ##### why
  - Faults in the pipeline will affect the internal pressure of the pipes.Therefore, internal pressure is a suitable indirect indicator for assessing the operational and structural integrity of the pipes.
- ##### the core of introduction 
  - a novel nonintrusive relative pressure sensor based on utilising low cost Force Sensitive Resistors
  - monitoring the temperature difference between the pipe wall and its surroundings and relative pressure sensors in order to detect pipe failure

#### 2. Theory of operation
As the internal pressure of a pipe changes the internal stress applied to the pipe wall will also change,the proposed sensing system indirectly uses this change in the radius to detect the changes of the internal pressure of the pipe.

The proposed relative pressure sensor assembly is composed of a stainless steel clip.As the change in the contact force is caused by the change in the internal pressure of the pipe the output of the FSR sensor can be related to the change in the pressure of the pipe.
![](/assets/8201.jpg)
###### Figure1 Schematic of the relative pressure sensor assembly
Equation 1 can be used to estimate the contact pressure PC between the pipe and the clip.

$$
Pc=  (P.r_p^2.E_j.t_j)/((r_p^2.E_j.t_j)+(r_j^2.E_p.t_p))------Equation 1
$$

Where $$P$$ is the internal pressure in the pipe; $$r_j$$and $$r_p$$ are the radii of the clip and the pipe; $$E_j$$ and $$E_p$$ are the respective material Young’s modulii of elasticity of the clip and pipe and $$t_j$$ and $$t_p$$ are the thickness of the clip and pipe respectively. 

Figure 2 and Figure 3 show the effect of pipe geometry on the applied contact pressure on the sensor for medium density polyethylene (MDPE) and cast iron pipes (at 1 kPa) respectively.
![](/assets/8202.jpg)


