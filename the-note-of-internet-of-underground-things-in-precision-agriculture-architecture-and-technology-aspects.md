### Internet of underground things in precision agriculture: Architecture and technology aspects

#### 0. Abstract

* Paper Detail
  * Vuran, M. C., et al. \(2018.7\). "Internet of underground things in precision agriculture: Architecture and technology aspects." Ad Hoc Networks 81: 160-173.
* Reason
  * increase in world population, increase in need for food
* Internet Of Underground Things\(IOUT\)
  * composition
    * sensors
    * communication devices
  * funtion
    * real-time soil sensing and monitoring
* Paper Content--IOUT
  * architectures
  * sensing
  * communication
  * technology
  * challenges 

#### 1. Introduction

* precision agricultures are widely adopted by farmers 
  * crop yield monitoring\ (61.4%\)
  * Variable Rate Technology \(VRT\) 
  * auto-steering system
  * crop moisture sensing
  
  ![](/assets/jpg1.jpg)

#### 2. Internet Of Underground Thing \(IOUT\)
- why
  - real-time in-situ information from agricultural fields
- what
  - autonomous devices that collect any relevant information about the Earth
  - communication and networks 
  - the growers and decision mechanisms
- Details
  - Communications can be carried out through the soil and plants from underground devices
  - Information acquired from the field can be sent to the cloud for real-time decision making
- Requirements--(wireless underground (UG) communications)
  - information from soil
  - operation in remote crop fields 
  - wireless communication through plants and soil
  - exposure to elements
- Benefit
  - conserve water resources and improve crop yields
  - landslide monitoring(滑坡监控) 
  - pipeline assessment
  - underground mining
  - border patrol（边境巡逻） 
  
#### 3. IOUT architecture
- Functionalities
  - In-situ sensing
    - soil moisture, temperature, salinity
  - Wireless communication in challenging environment
    -  adjust its parameters to adapt to dynamic changes in soil.
  - Inter-connection of field machinery, sensors, radios, and cloud
  - Real-time Decision Making
  - Mobility
- Components of the IOUT architecture
  - Underground things(UTs)
    - communication 
      -  Bluetooth, ZigBee, NFC, Wi-Fi
      - Sigfox, LoRa, LoRaWAN
      - satellite
      - cellular
    - sensing
      - soil temperature and moisture
    - weatherproof enclosures
    - power
      - solar panel
      - batteries
  - Base stations(transfer the collected data to the cloud)
  - Mobile sinks
    - tractors and irrigation systems
    - unmanned aerial vehicles
  - Cloud services
    - permanent storage of the data collected
    - real-time processing of the field condition
    - crop related decision making
    - integration with other databases

![](/assets/jpg2.jpg)
  
#### 4. Sensing
- Soil moisture(measure water content)
   - Gravimetric sampling(计重法采样)
     - how: a ratio of soil’s dry mass to the wet soil mass
     - requirement: manual sampling and oven drying of soil samples taken from the field
   - Resistive sensors
     - how: resistance changes based on soil water content
   - Capacitive sensors
     - how: changes in capacitance of soil due to water content variations
     - pros and cons: higher accuracy than resistive sensors but cost more
   - Ground Penetrating Radars 
     - how: the absorption and reflection of electromagnetic waves
     - requirement: measure near-surface soil moisture (up to 10 cm)
   - Neutron scattering probes and gauges(中子散射探头和仪表)
     - how: changes in neutron flux density due to the water content of the soil
     - pros and cons: most accurate but require specific licenses
   - Gamma ray attenuation
   - time-domain reflectometry (TDR)
   - frequency-domain reflectometry (FDR)

![](/assets/jpg3.jpg)

- Soil physical properties
  - the organic mater present in the soil（有机物）
  - acidity (pH)
  - percentage of sand, clay and silt particles
  - nutrients  
- Yield monitoring
  - make long-term decisions about agriculture operations
- Electrical conductivity and topography surveys
  - the amount of nitrogen usage (氮素用量)
  - water holding (持水量)
  - cation-exchange capacity (阳离子交换能力)
  - drainage (排水能力)
  - rooting depth (根生深度)
- Weather and environmental sensing
  - sense soil and air temperature
  - direction and speed of winds
  - rainfall, solar emissions and humidity
- Soil macro-nutrients sensing (the fertilizer impact and future applications)
  - nitrogen (氮), potassium (磷), phosphorous (钾)
  - Optical sensing
  - planar electromagnetic sensors (detect nitrate and sulfate concentration in natural water resources)
  - Electrochemical, VIS-NIRS spectroscopy, and ATR spectroscopy (电化学, VIS-NIRS光谱, ATR光谱)
- Remote sensing
  - electromagnetic waves which interact with soil and plants 
  - produce field maps for analysis and decision making based on in-situ IOUT sensing 
approaches
- precision agriculture technologies
  - precision planting
  - geolocation
  - GIS systems
  - soil sampling and field analysis map generation
  - drones
  - autosteering and VRT
  
#### 5. Wireless connectivity
- Challenges:lack of studies about the impacts of crops and farm environment on wireless propagation and associated tailored solutions to farms

#####5.1 In-field communications
- UG communications
  - benefit
    - complete concealment of UTs, which decrease operation costs and impacts from external elements 
  - two types of communication scenarios
    - Aboveground communication (between UTs and aboveground devices)
      - due to the soil-air interface, aboveground communication links are not symmetric 
    - Underground communication (between UTs) 
  - the path loss
    - underground link distances are still limited to 12 m
    - communication ranges of up to 200 m is possible for aboveground communications
    ![](/assets/jpg4.jpg)
  - six ways impact communication success 
    - Soil texture and bulk density
      - pore spaces, clay, sand, and silt particles (孔隙，黏土，沙子，淤泥)
      - Water holding capacity of each soil type is different because of its pore size
    - Soil moisture
      - diffusion attenuation
      - absorption by soil water content and its variations
    - Distance and depth variations
      - the soil-air interface(causes refraction of EM)
    - Antennas in soil
      - return loss characteristics change due to the high permittivity of soil 
    - Frequency variations
      - dipole relaxation associated with water(与水有关的偶极子弛豫)
      - at higher frequencies, water absorption plays a dominant role
    - Lateral waves
      - lateral, direct, and reflected (LDR) waves
      - lateral waves travel partly on the soil-air interface in air, experiencing the lowest attenuation
  - Recent advance
    - the characterization of wireless UG channel and development of environment-aware
      - Dong, X. and M. C. Vuran (2013). Environment aware connectivity for wireless underground sensor networks. 2013 Proceedings IEEE INFOCOM, IEEE.	
      - Salam, A. and M. C. Vuran (2016). Impacts of soil type and moisture on the capacity of multi-carrier modulation in internet of underground things. 2016 25th International Conference on Computer Communication and Networks (ICCCN), IEEE.
      - Salam, A., et al. (2016). Pulses in the sand: Impulse response analysis of wireless underground channel. IEEE INFOCOM 2016-The 35th Annual IEEE International Conference on Computer Communications, IEEE.
      - Salam, A., et al. (2017). Towards internet of underground things in smart lighting: A statistical model of wireless underground channel. 2017 IEEE 14th International Conference on Networking, Sensing and Control (ICNSC), IEEE.
      - Trang, H. T. H. and S. O. Hwang (2018). "Connectivity analysis of underground sensors in wireless underground sensor networks." Ad Hoc Networks 71: 104-116.
    - cross-layer communication solutions
      - Salam, A. and M. C. Vuran (2017). Wireless underground channel diversity reception with multiple antennas for internet of underground things. 2017 IEEE International Conference on Communications (ICC), IEEE.
      - Salam, A. and M. C. Vuran (2017). Smart underground antenna arrays: A soil moisture adaptive beamforming approach. IEEE INFOCOM 2017-IEEE Conference on Computer Communications, IEEE.
- Magnetic induction (MI) and acoustic UG communications
- Underground to UAV communications
- Low power wide area networks (LPWAN)
- Wireless PAN/LAN
- Cellular technology in IOUT
- Energy consumption in IOUT

#####5.2 Cloud and big data in precision agriculture

#### 6. IOUT enabling technologies
##### 6.1 Academic IOUT systems

* 6.1.1 Testbeds
* 6.1.2 Example 

##### 6.2 Commercial IOUT solutions

#### 7. Research challenges



