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
- Yield monitoring
- Electrical conductivity and topography surveys
- Weather and environmental sensing
- Soil macro-nutrients sensing
- Remote sensing

#### 5. Wireless connectivity
#####5.1 In-field communications
#####5.2 Cloud and big data in precision agriculture

#### 6. IOUT enabling technologies
##### 6.1 Academic IOUT systems

* 6.1.1 Testbeds
* 6.1.2 Example 

##### 6.2 Commercial IOUT solutions

#### 7. Research challenges



