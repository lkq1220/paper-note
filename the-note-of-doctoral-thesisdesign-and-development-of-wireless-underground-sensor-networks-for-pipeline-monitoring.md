### the note of doctoral thesis《DESIGN AND DEVELOPMENT OF WIRELESS UNDERGROUND SENSOR NETWORKS FOR PIPELINE MONITORING》

### 0. Abstract

a comprehensive review of the current state-of-the-art in pipeline monitoring is presented and the advantages and disadvantages of each of these methods are discussed. an ultra-low power Wireless Underground Sensor Network \(WUSN\) has been carefully researched, designed, developed and presented as part of this project.

* node communication
* power consumption\(by multiple iterations of software and hardware design\)
* data management\(dispensable\)
* sensor\(a novel non-invasive relative pressure sensor--FSR、temperature sensor\)
  * measure daily pressure variations
  * detect leak
  * leak detection position
* improved model for approximation of RF signal attenuation in soil

### 1. introductiom

#### 1.1 Background and motivation

Transportation of vital commodities such as water, oil and gas is commonly done by means of pipeline networks. Faults in these pipes can create major financial implications and possible environmental catastrophes.with the development of "Internet of Things",underground wireless sensor network not only provides operators with a better understanding of their network, but also will has a higher reliability and a faster response to faults.

##### The main method for detecting and locating leaks in pipe:

* acoustic measurements （声学）
* pressure measurements（压力）
* vision-based systems（计算机视觉）
* Ground Penetrating Radar \(GPR\) based systems （探地雷达）
* fibre optic monitoring（光纤检测）
* multimodal systems（多种模式）

##### the main issues in continuous infrastructure monitoring

* power consumption
* power availability
* sensor performance
  * power consumption
  * ease of installation 
  * cost and reliability
* data transmission

The focus of this research was on the single-hop \(star network\) WSN for pipeline monitoring\(星型网络实现节点通信\).This monitoring system contain many other sub-systems.

#### 1.2 Aim and objectives

The principal aim of this research is to design and manufacture a long-term, ultra low power continuous condition assessment monitoring system for buried water pipelines.

##### The following objectives:

\(1\) identify the parameters affecting the power consumption of underground wireless sensor nodes  
\(2\) design and manufacture an ultra-low power wireless sensor node for pipeline monitoring  
\(3\) minimise the power consumption of the node through hardware and software optimisation  
\(4\) design and develop non-invasive sensors and assess their performance  
\(5\) assess the performance of the node and sensors and assess leak detection capabilities of the system  
\(6\) investigate the effect of soil on Radio Frequency \(RF\) signal propagation--extraction of real and imaginary parts of permittivity from TDR waveform for use in prediction of RF attenuation in soil

### 2. Literature Review

#### 2.1 Pipline Systems

The ageing results in pipeline deterioration and eventually pipes failure, which can potentially have catastrophic financial and environmental effects.

* water supply network structure
  * Transmission networks
  * Distribution networks
  * water loss
    * distribution losses 
    * supply losses
* pipe materials\(currently plastic pipes are being nearly exclusively used for replacing and expanding existing water networks\)
  * cast iron
  * plastic\(colder environment and younger network\)
  * metallic
* pip ages
  * The average age of water pipeline networks is estimated to be approximately 50 years

#### 2.2 Pipeline deterioration process and failure

water pipes are exposed to harsh environmental and operational conditions which result in deteriorating and eventually failing.

##### two main categories of he deterioration of pipes

* Structural deteriorations
  * withstand operational and environmental loads
* Internal deteriorations
  * the hydraulic performance and water quality 

##### three main phases of the life cycle of the pipe

* Burn in \(the initial phase after installation of the pipe\)
  * human error
  * other installation issues 
  * manufacturing defects
* In usage\(longest\)
  * extreme operational/environmental conditions
  * external interferences
* Wear out
  * corrosion and degradation
    * Initiation of corrosion
    * Crack or hole before leak
    * Leak and scour begin 
    * Break or failure 

![](/assets/doctor1.jpg)

###### Figure1 Bathtub lifecycle of a pipeline.

![](/assets/doctor2.jpg)

###### Figure2 Stages of deterioration of the pipe

##### three main categories of factors affecting the deterioration process of water pipelines

* static
* dynamic\(Environmental factors\)
* operational factors\(maintenance and operation parameters of the pipeline networks\)

##### main reason for pipes failure

* In the literature corrosion is identified as the main reason for metallic pipes failure.
* The exertion of excessive forces
* Suffer from flaws in production
  * Porosity
  * inclusions
  * Micro cracks 
  * Variations in thickness 
* Human errors
  * Design 
  * Installation 
  * Operational errors    

##### two categories of Pipe failures

* burst\(a sudden failure of pipe\)
* leaks\(existing losses and losses which grow and develop over time\)

#### 2.2.1 Costs of failure and failure management

Failures in a pipe cause loss of the medium being transported by the pipe. Makar and Kleiner \(2000\) and Rajani and Kleiner \(2004\) divided the losses associated with a pipe failure in a water pipeline into three main categories of direct, indirect and social costs.  
![](/assets/doctor3.jpg)

###### Figure3  Categories of water pipe failure cost to asset owners

The total cost of failure management for water pipeline networks depends on the cost of the method used for condition assessment and leak detection.It is economical to use expensive leak detection and condition assessment techniques for water pipeline in order to detect failures.

#### 2.3 Pipeline condition assessment and failure monitoring systems

Failure management strategies can be divided into two main categories of passive and active techniques. In passive techniques the failure is identified based on consumer complaints \(low pressure and discoloured water\) or reports of water on the surface, while active techniques are intended to detect the failure before it reaches the stage in which it can be detected by passive techniques.  
Active failure management techniques are commonly referred to as Non-Destructive Testing\(NDT\).

* Non-Destructive Inspection \(NDI\) methods
* Non-Destructive Evaluation \(NDE\) methods

The main purpose of NDE methods is to evaluate the deterioration stage of the pipe without causing damage or affecting its properties.

* acoustic（声学）
  * Acoustic correlators
  * SAHARA technique（Synthetic Aperture High Altitude Radar 综合孔径高空雷达）
* electromagnetic（电子）
  * The Remote Field Eddy Current \(RFEC\) technique （远场涡流技术）
  * Magnetic flux leakage（漏磁）
  * Cround penetrating radar （探地雷达）
* ultra spectrum（超光谱）
  * Ultrasonic（超声）
  * Infrared thermography（红外热成像）
* physical\(物理\)
  * impact Echo（冲击回声）
  * Tracer gas （示踪气体）
* fibre optic （光纤）
  * local fibre optic sensor （本地光纤传感器）
  * Quasi-distributed fibre optic sensor（准分布式光纤传感器）
  * Distributed fibre optic sensor （分布式光纤传感器）
* visual（视觉）
  * CCTV inspection （闭路监控系统）
  * Laser based scanning（激光扫描）
* multi-sensor systems（多传感器系统）
  * Samrt pipe inspection gauges\(PIGS\)（智能管道检验）
  * Multi sensor underground wireless sensor network （多传感器地下无线传感网络） 

##### 2.3.1 Acoustic based methods

* Acoustic

  * Method: The frequency and magnitude of these signals depend on pipe pressure, leak diameter and type of fluid inside the pipe. These signals are detected by hydrophones\(水诊器\) or accelerometers（加速度计） placed at fixed location along the pipe.The location of the leak can then be calculated by cross-correlation methods applied on the signals measured by sensors at different locations.  
    ![](/assets/doctor5.jpg) 
    ###### Figure4 Schematic of an acoustic cross correlation leak detection system
  * Disadvantage：
    * requires a high sampling rate \(&gt;1KHz\),which makes the system consumes more power
    * be suited for metallic pipes, detection of vibrations in plastic pipes could be challenging  due to the higher attenuation of acoustic waves

* The SAHARA method

  * Method: be based on the detection of acoustic emission from the leaks. In the SAHARA method the hydrophone is inserted into the pipe with an umbilical cord via a conventional 50mm tap and records the acoustic signal as it travels through the pipe.

    ![](/assets/doctor6.jpg)

    ###### Figure5 SAHARA method and its components

  * Disadvantage：

    * need to travel through the pipe which jeopardises safety of the water supplies
    * limited by the diameter of the pipes in which it can effectively operate \(&gt;300mm\)

##### 2.3.2 Electromagnetic based methods

* Ground Penetrating Radar \(GPR\)
  * Method：Leaks in pipes are detected by GPR via detection of voids created by leaking water in the ground or abnormalities in the measured depth of the pipe due change of the soil attenuation due to change in local water content of soil 
  * Disadvantage
    * limited in more attenuative soils or deep assets due to a reduction in penetration depth of the signals
    * a skilled operator
    * require another form of verification to distinguish similar assets \(water and gas pipes\) due to the similar GPR signature of these assets
* Magnetic Flux Leakage \(MFL\)
  * Method: this method only suitable for clean steel pipes without interior lining.The pipe wall is magnetised using strong permanent magnets. A fault in the pipe will cause a magnetic flux leakage at the point of defect which can be detected by sensors.
    ![](/assets/doctor7.jpg)
    ###### Figure6 Schematic of the principal of Magnetic Flux Leakage \(MFL\) method
  * Disadvantage
    * unsuitable for older water pipes due to their tubercular interior surface
    * the potential damage to the lining of the pipe by the contacts used in these system 
* The Remote Field Eddy Current \(RFEC\)

  * Method: based on diffusion measurements of a low frequency electromagnetic signal at the  
    remote field zone travelling through the pipe wall.This system consists of excitation and  
    detection coils which are placed inside the pipe.Any changes in the wall thickness of the pipe shows itself as a change in the measured signal at the detector coils.

    ![](/assets/doctor8.jpg)

    ###### Figure7  Schematic of the principles of the remote field eddy current measurement method

  * Disadvantage

    * only be used with ferromagnetic pipes or pipe with ferromagnetic components 
    * limited information in the literature assesses the reliability of this method 

##### 2.3.3 Ultra spectrum based methods

* Ultrasonic methods

  * Method: As the sound wave travels through different materials it is reflected and scattered based on their densitiesTuberculation of metallic pipes will cause the signal to be scattered and therefore can be detected easily by this method. 

  ![](/assets/doctor9.jpg)

  ###### Figure8 Schematic of the ultrasonic pipe inspection method

  * Disadvantage
    * be mostly suited to metallic pipes due to the higher attenuation of the waves in the plastic pipes
    * the effectiveness of the systems is lost when defects in the pipe are small due to the magnitude of their reflections is smaller than noise bed of the system
    * Multiple overlapping reflections from similar features can also limit the effectiveness of this technique

* Infrared thermography

  * Method: This method is based on the detection of abnormalities in temperature of the soil around the pipe caused by the leakage of the medium being transferred by the pipe.In these systems a sensitive thermal imaging camera is used to capture the thermal profile of the soil and detect the local abnormalities.
  * Disadvantage
    * The performance of thermography based methods highly depends on a variety of conditions 

##### 2.3.4 Physical methods

* impact echo pipeline inspection 
  * Method: be based on generating controlled impact acoustic waves and measuring the propagated waves via geophones attached to the pipe wall. 
  * Disadvantage
    * the pipe needs to be dewatered and the internal surface of the pipes needs to be cleaned
* Tracer gas leak detection of pipes
  * Method: In the case of a defective pipe the gas will leak out from the pipe and travel upwards \(due to its low density\) through the ground and reach the soil surface. The marker gas can then be detected on the surface by sensitive gas detectors.
  * Disadvantage: high direct and indirect cost 

##### 2.3.5 Fibre optic based methods
- Advantage
  - passive operation (no need for local power supply)
  - large monitoring range
  - high spatial resolution
  - electromagnetic interference immunity
  - multiparameter sensing capabilities
- Fibre optic composition
  - fibre core (纤维芯)![
  - cladding（包层)](/assets/8243.jpg)
  - a jacket（夹层）
- Three main categories of Fibre optic system
  - Local (Point) Fibre optic systems
    - be suited for small-scale sensing
  - Quasi-distributed system(Fibre Bragg Grating (FBG) sensors)
    - large-scale multipoint measurement systems
  - Distributed systems
    - be best suited for large scale infrastructure monitoring(pipeline)
![](/assets/8241.jpg)
###### Figure 9 Schematic of different types of fibre optic monitoring systems. a) Local b) Quasi- distributed c) Distributed
- Disadvantage
 - Inherent lack of redundancy
 - Complex installation
 
##### 2.3.6 Visual (imaging) based methods Closed
- Closed circuit television (CCTV)
- Laser scanning systems (laser profilers)
- Disavantage
  - Require access to the interior of the pipe
  - Only operate in empty pipes

##### 2.3.7 Multi-sensor systems Smart
- Smart Pipe Inspection Gauge (PIG) systems
  - Method: Insert into the pipe through an opening and then travels through the pipe while recording its location and inspection data
  - Disadvantage
    - requires access to the interior of the pipes
    - cannot be used in smaller diameter (<150mm) pipes
- ##### Wireless Sensor Networks (WSN)*
 
#### 2.4 Wireless underground sensor networks for pipeline monitoring
##### 2.4.1 External systems 
- PIPENET
  - Figure 10 illustrates an overview of the PIPNET system
    - acoustic
    - water level
    - water quality 
    - pressure sensors
  ![](/assets/8242.jpg)
  ###### Figure 10 Overview of the PIPENET system
- WaterWise Platform
  - Figure 11 shows the WaterWise system
    - pressure
    - acoustic
    - water quality readings 
 ![](/assets/8243.jpg)
 ###### Figure 11 WaterWise system a) Multi parameter probe head b) installed WaterWise probe
- PipeTect
  - Method:
    - Sensor: vibration measurements (MEMS accelerometers) 
    - Communication: Wire connections for underground communication (CAN bus) and wireless communication (ZigBee and Wi-Fi) for overground communications
- MISE-PIPE
  - Figure 12 illustrates the overall schematic of the MISE-PIPE system
    - inside of the pipe
      - pressure
      - flow
      - acoustic vibrations
    - outside of the pipe 
      - temperature
      - humidity
      - soil properties
![](/assets/8244.jpg)
###### Figure 13 Overall schematic of the MISE-PIPE system
  - Advantage
    - use the Magnetic Induction (MI) technique to overcome the Challenges of signal propagation in soil
  - Disadvantage
    - this claim is only valid for non-magnetic soils
    - magnetic waves compared to EM waves is that their intensity drops with distance significantly faster than EM waves. 
    - the cost of installation 
    - high-energy consumption

##### 2.4.2 Internal systems
- The TriopusNet system
  - Figure 14 shows the prototype of the TriopusNet node
  ![](/assets/8245.jpg)
  ###### Figure 14 Prototype of the TriopusNet node

##### 2.4.3 RF progation in soil
- Two main models for the prediction of EM wave attenuation in soil
  - CRIM-Fresnel model
  - Modified Friis model
- EM wave propagation in free space
$$
P_r(d)=  (P_t G_t G_r λ ^2)/(4π)^2 d^2 
$$
Where $$P_t$$ is the transmitter power, $$G_t$$ and $$G_r$$ are the transmitter and receiver antenna gains,and d is the distance between the transmitter and receiver and λ is the wavelength of the EM wave in open space.
- EM wave propagation in soil based on modified-Friis model

