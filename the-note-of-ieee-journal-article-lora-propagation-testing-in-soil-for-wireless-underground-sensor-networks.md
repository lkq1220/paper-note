## the note of IEEE journal article 《LoRa Propagation Testing in Soil for Wireless Underground Sensor Networks》

### 0. Abstract
LoRa provides new in-soil propagation means for wireless sensor networks with some node buried underground.The LoRa propagation characteristics related to volumetric water content, burial depth and payload are experimentally evaluated with the testing node.The test results shows that the packet success rate based LoRa in-soil propagation evaluations can be obtained by the testnode.

### 1. Introduction
- #### WUSN
  - ##### WUSN Introduction： WUSNs are sensor networks that comprise wireless underground sensor devices, which send and receive data or instructions in the soil
  - ##### WUSN Application Fields
    - agriculture
    - accident prevention
    - security
    - transportation
    - structural engineering
    - earth science
  - ##### The Challenge Of WUSN
    - WUSNs are immature
    - The in-soil propagation loss of radio signal is key bottleneck for WUSNs 
      - the soil type
      - soil moisture
      - underground obstructions(refraction and scattering of radio signals)
- #### LoRa
  - ##### LoRa Introduction: which stands for “Long Range” , which is design for Low Power Wide Area Network (LPWAN) specification
  - ##### LoRa Advantage
    - chirp spread spectrum modulation(线性调频扩频调制)
    - immune to the Doppler effect（对多普勒效应免疫）
    - offer sensitivity of the order of −130 dBm
    - long propagation distance
    - energy consumption, long battery-powered life, simple star-of-stars topology,easy configuration and low cost.
  - ##### LoRa Channel Characteristics
    - Due to the soil type, the LoRa channel characteristics between nodes in different environments usually show large differences.So the in-soil LoRa channel characteristics and data transmission effect should be obtained by actual measurement
    
### 2. Desgin of Testnode
- #### PSR(the packet success rate)
  - Because LoRa modulation in physical layer is a Semtech(升特) Corporation proprietary technology and is as such not fully open.So we So we use the packet success rate (PSR) as the key evaluation criterion of LoRa propagation performance.PSR is defined as the percentage of packets that transmit successfully ($$P_s$$) to total packets ($$P_t$$):
  $$
  PSR=p_s/p_t×100percent
  $$
- #### Desgin 
  - twin testnode configuration are adopt for measurement as shown in Figure 1.
  ![](/assets/8211.jpg)
  ###### Figure 1. Measurement system configuration
  
- ####Testnode 
![](/assets/8212.jpg)
###### Figure 2. Schematic of the Testnode 

### 3. Test Result And Discussion
- #### 

### 4. Conclusion
- #### LoRa Advantage
    - high sensitivity
    - spread spectrum
    - low Doppler effect
- #### LoRa Propagation Characteristics