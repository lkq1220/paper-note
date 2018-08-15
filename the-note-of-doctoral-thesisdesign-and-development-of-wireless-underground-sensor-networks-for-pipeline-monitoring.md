### the note of doctoral thesis《DESIGN AND DEVELOPMENT OF WIRELESS UNDERGROUND SENSOR NETWORKS FOR PIPELINE MONITORING》

### 0. Abstract
a comprehensive review of the current state-of-the-art in pipeline monitoring is presented and the advantages and disadvantages of each of these methods are discussed. an ultra-low power Wireless Underground Sensor Network (WUSN) has been carefully researched, designed, developed and presented as part of this project.
- node communication
- power consumption(by multiple iterations of software and hardware design)
- data management(dispensable)
- sensor(a novel non-invasive relative pressure sensor--FSR、temperature sensor)
    -  measure daily pressure variations
    -  detect leak
    -  leak detection position
- improved model for approximation of RF signal attenuation in soil

### 1. introductiom
#### 1.1 Background and motivation 
Transportation of vital commodities such as water, oil and gas is commonly done by means of pipeline networks. Faults in these pipes can create major financial implications and possible environmental catastrophes.with the development of "Internet of Things",underground wireless sensor network not only provides operators with a better understanding of their network, but also will has a higher reliability and a faster response to faults. 

##### The main method for detecting and locating leaks in pipe:
- acoustic measurements （声学）
- pressure measurements（压力）
- vision-based systems（计算机视觉）
- Ground Penetrating Radar (GPR) based systems （探地雷达）
- fibre optic monitoring（光纤检测）
- multimodal systems（多种模式）

##### the main issues in continuous infrastructure monitoring
- power consumption
- power availability
- sensor performance
    - power consumption
    - ease of installation 
    - cost and reliability
- data transmission

The focus of this research was on the single-hop (star network) WSN for pipeline monitoring(星型网络实现节点通信).This monitoring system contain many other sub-systems.

#### 1.2 Aim and objectives
The principal aim of this research is to design and manufacture a long-term, ultra low power continuous condition assessment monitoring system for buried water pipelines.
##### The following objectives:
(1) identify the parameters affecting the power consumption of underground wireless sensor nodes
(2) design and manufacture an ultra-low power wireless sensor node for pipeline monitoring
(3) minimise the power consumption of the node through hardware and software optimisation
(4) design and develop non-invasive sensors and assess their performance
(5) assess the performance of the node and sensors and assess leak detection capabilities of the system
(6) investigate the effect of soil on Radio Frequency (RF) signal propagation--extraction of real and imaginary parts of permittivity from TDR waveform for use in prediction of RF attenuation in soil 

### 2. Literature Review
#### 2.1 Pipline Systems
The ageing results in pipeline deterioration and eventually pipes failure, which can potentially have catastrophic financial and environmental effects.
- water supply network structure
    - Transmission networks
    - Distribution networks
    - water loss
        - distribution losses 
        - supply losses
- pipe materials(currently plastic pipes are being nearly exclusively used for replacing and expanding existing water networks)
    - cast iron
    - plastic(colder environment and younger network)
    - metallic
- pip ages
    - The average age of water pipeline networks is estimated to be approximately 50 years
    
#### 2.2 Pipeline deterioration process and failure
water pipes are exposed to harsh environmental and operational conditions which result in deteriorating and eventually failing.
##### two main categories of he deterioration of pipes
- Structural deteriorations
    - withstand operational and environmental loads
- Internal deteriorations
    - the hydraulic performance and water quality 
    
##### three main phases of the life cycle of the pipe
- Burn in (the initial phase after installation of the pipe)
    - human error
    - other installation issues 
    - manufacturing defects
- In usage(longest)
    - extreme operational/environmental conditions
    - external interferences
- Wear out
    - corrosion and degradation
        - Initiation of corrosion
        - Crack or hole before leak
        - Leak and scour begin 
        - Break or failure 

![](/assets/doctor1.jpg)
###### Figure1 Bathtub lifecycle of a pipeline. 
![](/assets/doctor2.jpg)
###### Figure2 Stages of deterioration of the pipe

##### three main categories of factors affecting the deterioration process of water pipelines
- static
- dynamic(Environmental factors)
- operational factors(maintenance and operation parameters of the pipeline networks)

##### main reason for pipes failure 
- In the literature corrosion is identified as the main reason for metallic pipes failure.
- The exertion of excessive forces
- Suffer from flaws in production
    - Porosity
    - inclusions
    - Micro cracks 
    - Variations in thickness 
- Human errors
    - Design 
    - Installation 
    - Operational errors    
    
##### two categories of Pipe failures 
- burst(a sudden failure of pipe)
- leaks(existing losses and losses which grow and develop over time)
    
#### 2.2.1 Costs of failure and failure management
Failures in a pipe cause loss of the medium being transported by the pipe. Makar and Kleiner (2000) and Rajani and Kleiner (2004) divided the losses associated with a pipe failure in a water pipeline into three main categories of direct, indirect and social costs.
![](/assets/doctor3.jpg)
##### Figure3  Categories of water pipe failure cost to asset owners

#### 2.3 Pipeline condition assessment and failure monitoring systems
#### 2.4 Wireless underground sensor networks for pipeline monitoring




