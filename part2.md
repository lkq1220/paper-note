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
- Energy resource
  - limited
  - non-replenshable
- A typical routine for infrastructure monitoring
  - measurement
  - process
  - receive
  - transmission
  - sleep
- The major tasks undertaken at each mode are illustrated in Figure 4
![](/assets/8249.jpg)
###### Figure 4 WUSN operation modes and the major tasks undertaken at each mode
- the method of reducing the power consumption 
  - faster sensor with lower consumption 
  - optimise the MCU processing speed
- Main factors affecting the power consumption during different operational modes of each node
###### Table 1 Main factors affecting the power consumption during different operational modes of each node.
![](/assets/8250.jpg)
- The average power consumption of the node $$P_Av$$" depends on the power consumption and
duration of all of the operational modes of the node. 
$$
P_Av = ((T_m*P_m)+(T_tx*P_tx)(T_total-T_tx-T_m)*P_sleep)/T_total
$$
  - $$T_m$$ is the duration of measurements and processing
  - $$P_m$$ is the power consumption of the node during measurement and processing
  - $$T_tx$$ is is the duration for which the transmitter is on
  - $$P_tx$$ is the power consumption of the node during transmission mode
  - $$p_sleep$$ is the power consumption of the node during sleep mode
  - $$T_total$$ is the transmission interval
-  Figure 5 illustrates the theoretical average power consumption of a node based on the
measurement frequency
![](/assets/8251.jpg)
######Figure 5 Theoretical power consumption of the node based on measurement frequency Based on the assumed power consumption during sleep of 3.3µW and operational power consumption of 75mW (operational duration of 500ms).
- In pipelines, faults usually develop slowly which enables the pipeline monitoring system to operate at lower measurement frequencies.
- Equation (3.2) can be used for calculating the average power consumption of the node based on different transmission and measurement rates
![](/assets/8252.jpg) （3.2）
- Figure6 illustrates the effect of the measurement frequency on power consumption based on Equation (3.2) for different transmission intervals.
![](/assets/8253.jpg)
###### Figure 6  Effect of measurement interval on average power consumption
-  a transmission interval of 8 hours with a measurement interval of 30 minutes is selected for
this pipeline monitoring
- Figure 7a, illustrates the power consumption of the node during each mode, while Figure 7b illustrates the total energy consumed by the node during each mode for one full cycle (2 hour transmission interval).
![](/assets/8254.jpg)
###### Figure 7 (a) Power consumption of the node during each mode, (b) Total energy consumed by the node during each mode for one full cycle (2 hour transmission interval)
- the method for minimising the overall comsumed energy
  - reduce the duration
  - decrease the power consumption of node

##### 3.2.3 Hardware design
- The main objective of the design
  - Ultra-low power consumption
  - Good RF performance (min 0dBm) and flexibility in operational frequency
  - Adequate connectivity
  - Low cost
  - Small size
- Table 2 shows the main limitations and improvements of each of the iterations of the node.
###### Table 2 Comparison of the limitations and improvements made for each of the iterations of the node
![](/assets/8255.jpg)
-Table 3 illustrates the specification of Version 2.0 of the node
###### Table 3 Specification of version 2.0 of the node
![](/assets/8256.jpg)  
- An SMA antenna connector
- A ground plane
  - reduce the noise due to cross talk and interference 
- A mini USB port
- The power management module
  - Figure 8 illustrates the schematic of the power management module of this version of the node
![](/assets/8257.jpg)
###### Figure 7 Schematic of the power regulator module for version 2.0 of the node
    - Mode1(2-5.5V) for Li-Ion batteries and solar cells
    - Mode2(3.3-16V) for piezoelectric harvesters.
    - Mode3 for thin film batteries
    - Mode4(2.5-16V) support two constant voltage supplies of 1.8V or 3V

##### 3.2.4 Firmware design 
- The main Main MCU parameters which affect the firmware design and performance
  - Processing Power
  - Sleep instruction
  - Communication speed
- A detailed description of each of the steps carried out by the firmware of the node is as follows:
  1. initial peripheral hardware module
  2. initial and define variable and counters
  3. set the signal of LED
  4. connect sensors
  5. measure the data of sensor according to the exchange of Analogue/Digital
  6. power down the sensor
  7. data process(transform the sensors’ raw output into a usable form)
  8. The results are compared with the adaptive thresholds for each parameter and flags are
set if necessary
  9. pack transmission data(the result/node unique identifier/transmission identifier)
  10. initial UART Module
  11. power on the transceiver module
  12. a short delay(in order to make the status of UART module suitable)
  13. The transceiver stays in listening mode for a set period of time waiting for data from
other nodes 
  14. received data is processed and  if required is packaged with local data (only applicable for data router nodes).
  15. The packaged data is transferred to the buffer of the transceiver
  16. Data is transmitted by the transceiver
  17. The transceiver is powered down
  18. Sleep instructions are performed in order to put the MCU in deep sleep with a WDT
wake up
  19. The MCU is woken up from deep sleep by the WDT
  20. The timer counter is checked; if the correct sleep time is reached the program goes to
step 4, if not, the counter is increased and the program goes to step 18.
- two main challenges in the design of the firmware for WUSN
  - Reduction in overall “ON” time
  - the accuracy of timing


#### 3.3 Summary
- ##### The most desirable specification for a successful WUSN for pipeline monitoring
  - Ease of installation
  - Low cost
  - Long operational life(low power consumption)
    - The sleep mode was identified as the main consumer of the total energy
    - An increase in the operational frequency of the MCU will result in a reduction of the ON duration and consequently a reduction in overall power consumption
    - The final version of the developed node had an extremely low average power consumption of 1.31 µW for one measurement and transmission every six hours
  - Non-invastive to the structure of the pipe
 