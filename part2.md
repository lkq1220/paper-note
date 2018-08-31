### Design and development of wireless underground sensor network for pipeline monitoring
#### 3.1 Introduction
- ##### Figure 1 illustrates the main limitations and requirements for a WUSN for pipeline monitoring systems
![](/assets/8246.jpg)
###### Figure 1 Limitations and requirements of WUSN for pipeline monitoring
- Environment limitation
  - High RF signal
  - Lake of maintainablity
  - Lake of access to the power supply
  - Harsh environment
- Application requirements
  - Ease of installation
  - Low cost
  - Long operational life
  - Non-invastive to the structure of the pipe
  - Capable of detecting abnormalities in pipes
  
#### 3.2 System structure
- Figure 2 illustrates the typical schematic of a wireless sensor network for pipeline monitoring
![](/assets/8247.jpg)
###### Figure 2 Schematic of a wireless sensor network for pipeline monitoring
- The overall architecture of the WUSN for pipeline monitoring
  - Sensor node
    - pipe temperature
    - soil temperature
    - pipe internal pressure 
    - soil water content
  - Master node
  - Cloud Server
  - End user
- Figure 3 shows a typical data flow in a WUSN for pipeline monitoring
![](/assets/8248.jpg)
###### Figure 3 Typical data flow in a WUSN between network layers

##### 3.2.1 Node design overview 
- Four main subsystems for the hardware WUSN node 
  - Microcontroller Unit (MCU)
    - gathering the data
    - process data
    - run the leak detection algorithms
    - buffer data into the tranceiver
    - time
    - ultra-low power microcontroller 
  - transceiver
    - send data to the mater node
  - power management
    - condition and manage the supplied power
  - signal conditioning 
    - A/D Conversion
    
##### 3.2.2 Power consumption

##### 3.2.3 Hardware design

##### 3.2.4 Firmware design

#### 3.3 Summary
- ##### The most desirable specification for a successful WUSN for pipeline monitoring
  - Ease of installation
  - Low cost
  - Long operational life(low power consumption)
    - The sleep mode was identified as the main consumer of the total energy
    - An increase in the operational frequency of the MCU will result in a reduction of the ON duration and consequently a reduction in overall power consumption
    - The final version of the developed node had an extremely low average power consumption of 1.31 µW for one measurement and transmission every six hours
  - Non-invastive to the structure of the pipe
 